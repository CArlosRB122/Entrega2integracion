pipeline {
    agent any // Usa cualquier agente disponible
    stages {
        stage('Clonar código') {
            steps {
                echo 'Descargando código del repositorio...'
                checkout scm // Clona el código del repositorio configurado
            }
        }
        stage('Compilación') {
            steps {
                echo 'Compilando código...'
                sh 'mvn clean compile' // Cambia este comando según tu tecnología (npm, gradle, etc.)
            }
        }
        stage('Pruebas') {
            steps {
                echo 'Ejecutando pruebas...'
                sh 'mvn test' // Ejecuta tus pruebas automáticas
            }
        }
    }
    post {
        success {
            echo '¡Pipeline completado exitosamente!'
        }
        failure {
            echo 'Algo salió mal durante la ejecución del pipeline.'
        }
    }
}
