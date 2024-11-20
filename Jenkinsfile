pipeline {
    agent any

    tools {
        maven 'Maven3'  
    }

    stages {
        stage('Preparación') {
            steps {
                echo 'Preparando el entorno...'
            }
        }

        stage('Clonar código') {
            steps {
                echo 'Clonando el código...'
                checkout scm
            }
        }

        stage('Instalar dependencias') {
            steps {
                echo 'Instalando dependencias...'
                bat 'mvn install'
            }
        }

        stage('Compilación') {
            steps {
                echo 'Compilando el proyecto...'
                bat 'mvn compile'
            }
        }

        stage('Pruebas') {
            steps {
                echo 'Ejecutando pruebas...'
                bat 'mvn test'
            }
        }

        stage('Despliegue') {
            steps {
                echo 'Desplegando la aplicación...'
                bat 'mvn deploy'
            }
        }
    }
}

