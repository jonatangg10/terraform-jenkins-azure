<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>

pipeline {
    agent any
    
    environment {
        AZURE_CREDENTIALS_ID = 'azure-credentials'
    }
    
    stages {
        stage('Print Azure Credentials') {
            steps {
                script {
                    withCredentials([azureServicePrincipal(credentialsId: AZURE_CREDENTIALS_ID)]) {
                        echo "Client ID: $AZURE_CLIENT_ID"
                        echo "Client Secret: $AZURE_CLIENT_SECRET"
                        echo "Tenant ID: $AZURE_TENANT_ID"
                        echo "Subscription ID: $AZURE_SUBSCRIPTION_ID"
                    }
                }
            }
        }
    }
}
