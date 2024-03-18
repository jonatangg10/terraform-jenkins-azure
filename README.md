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
        stage('Azure Login') {
            steps {
                script {
                    withCredentials([azureServicePrincipal(credentialsId: AZURE_CREDENTIALS_ID, tenantId: 'TENANT_ID')]) {
                        sh 'az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET --tenant $AZURE_TENANT_ID'
                    }
                }
            }
        }
        
        stage('Azure Show') {
            steps {
                script {
                    sh 'az account show'
                }
            }
        }
        
        stage('Azure Logout') {
            steps {
                script {
                    sh 'az logout'
                }
            }
        }
    }
}
