<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>

pipeline {
    agent any

    stages {
        stage('Print Azure Credentials') {
            steps {
                script {
                    // Utilizar las credenciales de Azure CLI
                    withCredentials([usernamePassword(credentialsId: 'azure', usernameVariable: 'AZURE_USERNAME', passwordVariable: 'AZURE_PASSWORD')]) {
                        // Autenticar con Azure CLI
                        sh "az login --username $AZURE_USERNAME --password $AZURE_PASSWORD"

                        // Mostrar información de la cuenta de Azure
                        sh "az account show"
                    }
                }
            }
        }
    }

    post {
        always {
            // Cerrar sesión de Azure CLI después de ejecutar el pipeline
            sh "az logout"
        }
    }
}
