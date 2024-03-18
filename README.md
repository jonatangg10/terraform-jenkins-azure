<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>
22:06:55  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
22:06:55  [Pipeline] Start of Pipeline
22:06:55  [Pipeline] node
22:06:55  Running on jonatan in /var/jenkins_home/workspace/prueba-azure
22:06:55  [Pipeline] {
22:06:55  [Pipeline] stage
22:06:55  [Pipeline] { (Print Azure Credentials)
22:06:55  [Pipeline] script
22:06:55  [Pipeline] {
22:06:56  [Pipeline] withCredentials
22:06:56  Masking supported pattern matches of $AZURE_SUBSCRIPTION_ID or $AZURE_TENANT_ID or $AZURE_CLIENT_SECRET or $AZURE_CLIENT_ID
22:06:56  [Pipeline] {
22:06:56  [Pipeline] sh
22:06:56  Warning: A secret was passed to "sh" using Groovy String interpolation, which is insecure.
22:06:56  		 Affected argument(s) used the following variable(s): [AZURE_TENANT_ID, AZURE_CLIENT_SECRET, AZURE_CLIENT_ID]
22:06:56  		 See https://jenkins.io/redirect/groovy-string-interpolation for details.
22:06:56  + az login --service-principal -u **** -p **** --tenant ****
22:06:58  ERROR: No subscriptions found for ****.
22:06:58  [Pipeline] }
22:06:58  [Pipeline] // withCredentials
22:06:58  [Pipeline] }
22:06:58  [Pipeline] // script
22:06:58  [Pipeline] }
22:06:58  [Pipeline] // stage
22:06:58  [Pipeline] stage
22:06:58  [Pipeline] { (Declarative: Post Actions)
22:06:58  [Pipeline] sh
22:06:59  + az logout
22:06:59  ERROR: There are no active accounts.
22:06:59  Error when executing always post condition:
22:06:59  Also:   org.jenkinsci.plugins.workflow.actions.ErrorAction$ErrorId: 72a055ae-7bec-46c7-880b-38d646bf0fa0
22:06:59  hudson.AbortException: script returned exit code 1
22:06:59  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.handleExit(DurableTaskStep.java:668)
22:06:59  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.check(DurableTaskStep.java:614)
22:06:59  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.run(DurableTaskStep.java:555)
22:06:59  	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:539)
22:06:59  	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
22:06:59  	at java.base/java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304)
22:06:59  	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1136)
22:06:59  	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:635)
22:06:59  	at java.base/java.lang.Thread.run(Thread.java:840)
22:06:59  
22:06:59  [Pipeline] }
22:06:59  [Pipeline] // stage
22:06:59  [Pipeline] }
22:06:59  [Pipeline] // node
22:06:59  [Pipeline] End of Pipeline
22:06:59  ERROR: script returned exit code 1
22:06:59  Finished: FAILURE
