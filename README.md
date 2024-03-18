<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>

23:22:16  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
23:22:16  [Pipeline] Start of Pipeline
23:22:17  [Pipeline] node
23:22:17  Running on Jenkins  in /var/jenkins_home/workspace/prueba-azure2
23:22:17  [Pipeline] {
23:22:17  [Pipeline] withEnv
23:22:17  [Pipeline] {
23:22:17  [Pipeline] stage
23:22:17  [Pipeline] { (Azure Login)
23:22:17  [Pipeline] script
23:22:17  [Pipeline] {
23:22:17  [Pipeline] withCredentials
23:22:17  Masking supported pattern matches of $AZURE_SUBSCRIPTION_ID or $AZURE_TENANT_ID or $AZURE_CLIENT_SECRET or $AZURE_CLIENT_ID
23:22:17  [Pipeline] {
23:22:17  [Pipeline] sh
23:22:17  + az login --service-principal
23:22:18  ERROR: usage error: --service-principal --username NAME --password SECRET --tenant TENANT
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // withCredentials
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // script
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // stage
23:22:18  [Pipeline] stage
23:22:18  [Pipeline] { (Azure Show)
23:22:18  Stage "Azure Show" skipped due to earlier failure(s)
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // stage
23:22:18  [Pipeline] stage
23:22:18  [Pipeline] { (Azure Logout)
23:22:18  Stage "Azure Logout" skipped due to earlier failure(s)
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // stage
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // withEnv
23:22:18  [Pipeline] }
23:22:18  [Pipeline] // node
23:22:18  [Pipeline] End of Pipeline
23:22:18  ERROR: script returned exit code 1
23:22:18  Finished: FAILURE

