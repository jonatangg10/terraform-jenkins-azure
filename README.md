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
                    // Utilizar las credenciales de Azure Service Principal
                    withCredentials([azureServicePrincipal(credentialsId: 'azure', 
                            tenantIdVariable: 'AZURE_TENANT_ID',
                            clientIdVariable: 'AZURE_CLIENT_ID',
                            clientSecretVariable: 'AZURE_CLIENT_SECRET')]) {
                        // Autenticar con Azure CLI usando la credencial de Azure Service Principal
                        sh "az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET --tenant $AZURE_TENANT_ID"

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
