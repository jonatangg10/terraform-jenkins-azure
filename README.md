<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>

pipeline {
    agent any

    parameters {
        string(name: 'clientId', description: 'Azure Client ID')
        string(name: 'clientSecret', description: 'Azure Client Secret', defaultValue: '', /* secret: true */)
        string(name: 'tenantId', description: 'Azure Tenant ID')
        string(name: 'subscriptionId', description: 'Azure Subscription ID')
    }

    stages {
        stage('Print Azure Credentials') {
            steps {
                script {
                    // Configurar las credenciales de Azure CLI
                    withCredentials([
                        usernamePassword(credentialsId: 'azure-cli-credentials', usernameVariable: 'azUsername', passwordVariable: 'azPassword')
                    ]) {
                        // Autenticar con Azure CLI
                        sh "az login --service-principal --username $clientId --password $clientSecret --tenant $tenantId"

                        // Establecer la suscripción activa
                        sh "az account set --subscription $subscriptionId"

                        // Mostrar información de la cuenta
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
