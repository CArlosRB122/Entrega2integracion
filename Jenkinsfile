pipeline {
    agent any

    stages {
        stage('Preparación') {
            steps {
                echo 'Preparando el entorno...'
            }
        }
        
        stage('Clonar código') {
            steps {
                checkout scm
            }
        }

        stage('Instalar dependencias') {
            steps {
                echo 'Instalando dependencias...'
                sh 'mvn install'
            }
        }

        stage('Compilación') {
            steps {
                echo 'Compilando el proyecto...'
                sh 'mvn compile'
            }
        }

        stage('Pruebas') {
            steps {
                echo 'Ejecutando pruebas...'
                sh 'mvn test'
            }
        }

        stage('Despliegue') {
            steps {
                echo 'Desplegando la aplicación...'
                sh 'mvn deploy'
            }
        }
    }
}

