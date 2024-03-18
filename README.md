<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>
22:44:56  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
22:44:56  [Pipeline] Start of Pipeline
22:44:56  [Pipeline] node
22:44:56  Running on jonatan in /var/jenkins_home/workspace/prueba-azure
22:44:56  [Pipeline] {
22:44:56  [Pipeline] withEnv
22:44:56  [Pipeline] {
22:44:56  [Pipeline] stage
22:44:56  [Pipeline] { (Azure Login)
22:44:56  [Pipeline] script
22:44:56  [Pipeline] {
22:44:56  [Pipeline] withCredentials
22:44:56  WARNING: Unknown parameter(s) found for class type 'com.microsoft.azure.util.AzureCredentialsBinding': tenantId
22:44:56  Masking supported pattern matches of $AZURE_SUBSCRIPTION_ID or $AZURE_TENANT_ID or $AZURE_CLIENT_SECRET or $AZURE_CLIENT_ID
22:44:56  [Pipeline] {
22:44:56  [Pipeline] sh
22:44:56  + az login --service-principal -u **** -p **** --tenant ****
22:44:59  ERROR: No subscriptions found for ****.
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // withCredentials
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // script
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // stage
22:44:59  [Pipeline] stage
22:44:59  [Pipeline] { (Azure Show)
22:44:59  Stage "Azure Show" skipped due to earlier failure(s)
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // stage
22:44:59  [Pipeline] stage
22:44:59  [Pipeline] { (Azure Logout)
22:44:59  Stage "Azure Logout" skipped due to earlier failure(s)
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // stage
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // withEnv
22:44:59  [Pipeline] }
22:44:59  [Pipeline] // node
22:44:59  [Pipeline] End of Pipeline
22:44:59  ERROR: script returned exit code 1
22:44:59  Finished: FAILURE
