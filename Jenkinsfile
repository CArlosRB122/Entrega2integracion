pipeline {
    agent any
    tools {
        maven 'Maven'  // El nombre que has dado a la instalación de Maven en Jenkins
    }
    stages {
        stage('Instalar dependencias') {
            steps {
                sh 'mvn dependency:resolve'  // Usar el comando Maven
            }
        }
        stage('Compilación') {
            steps {
                sh 'mvn compile'  // Compilar el código
            }
        }
        stage('Pruebas') {
            steps {
                sh 'mvn test'  // Ejecutar pruebas
            }
        }
        stage('Empaquetar artefactos') {
            steps {
                sh 'mvn package'  // Empaquetar artefactos
            }
        }
        stage('Despliegue') {
            steps {
                // Despliegue si es necesario
            }
        }
    }
}
}
