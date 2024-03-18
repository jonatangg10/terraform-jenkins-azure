<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>
23:26:05  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
23:26:05  [Pipeline] Start of Pipeline
23:26:05  [Pipeline] node
23:26:05  Running on Jenkins  in /var/jenkins_home/workspace/prueba-azure2
23:26:05  [Pipeline] {
23:26:05  [Pipeline] withEnv
23:26:05  [Pipeline] {
23:26:05  [Pipeline] stage
23:26:05  [Pipeline] { (Azure Login)
23:26:05  [Pipeline] script
23:26:05  [Pipeline] {
23:26:05  [Pipeline] withCredentials
23:26:05  Masking supported pattern matches of $AZURE_SUBSCRIPTION_ID or $AZURE_TENANT_ID or $AZURE_CLIENT_SECRET or $AZURE_CLIENT_ID
23:26:05  [Pipeline] {
23:26:05  [Pipeline] sh
23:26:05  Warning: A secret was passed to "sh" using Groovy String interpolation, which is insecure.
23:26:05  		 Affected argument(s) used the following variable(s): [AZURE_TENANT_ID, AZURE_CLIENT_SECRET, AZURE_CLIENT_ID]
23:26:05  		 See https://jenkins.io/redirect/groovy-string-interpolation for details.
23:26:05  + az login --service-principal --username **** --password **** --tenant ****
23:26:07  ERROR: No subscriptions found for ****.
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // withCredentials
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // script
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // stage
23:26:07  [Pipeline] stage
23:26:07  [Pipeline] { (Azure Show)
23:26:07  Stage "Azure Show" skipped due to earlier failure(s)
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // stage
23:26:07  [Pipeline] stage
23:26:07  [Pipeline] { (Azure Logout)
23:26:07  Stage "Azure Logout" skipped due to earlier failure(s)
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // stage
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // withEnv
23:26:07  [Pipeline] }
23:26:07  [Pipeline] // node
23:26:07  [Pipeline] End of Pipeline
23:26:07  ERROR: script returned exit code 1
23:26:07  Finished: FAILURE
