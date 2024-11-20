pipeline {
    agent any // Usa cualquier agente disponible

    stages {
        stage('Preparación') {
            steps {
                echo 'Preparando entorno para el pipeline...'
                // Configuraciones iniciales, si las necesitas
            }
        }
        stage('Clonar código') {
            steps {
                echo 'Descargando código del repositorio...'
                // Clona el código desde el repositorio configurado en Jenkins
                checkout scm
            }
        }
        stage('Instalación de dependencias') {
            steps {
                echo 'Instalando dependencias necesarias...'
                // Ajusta este comando según tu tecnología (npm, pip, composer, etc.)
                bat 'mvn dependency:resolve' // Ejemplo para Maven
            }
        }
        stage('Compilación') {
            steps {
                echo 'Compilando código...'
                // Cambia el comando según la tecnología que estés usando
                bat 'mvn clean compile'
            }
        }
        stage('Pruebas') {
            steps {
                echo 'Ejecutando pruebas...'
                // Ajusta el comando para ejecutar tus pruebas
                bat 'mvn test'
            }
        }
        stage('Empaquetar artefactos') {
            steps {
                echo 'Generando artefactos...'
                // Cambia el comando para crear los artefactos según tu tecnología
                bat 'mvn package'
            }
        }
        stage('Despliegue') {
            steps {
                echo 'Desplegando aplicación...'
                // Agrega aquí el comando para desplegar la aplicación
                bat 'echo Comando de despliegue aquí'
            }
        }
    }

    post {
        success {
            echo '¡Pipeline completado exitosamente!'
        }
        failure {
            echo 'Hubo un error en el pipeline. Revisa los logs para más detalles.'
        }
        always {
            echo 'Pipeline finalizado.'
            // Aquí puedes agregar comandos adicionales, como notificaciones
        }
    }
}
