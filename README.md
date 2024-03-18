<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>

22:04:33  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
22:04:33  [Pipeline] Start of Pipeline
22:04:33  [Pipeline] node
22:04:33  Running on jonatan in /var/jenkins_home/workspace/prueba-azure
22:04:33  [Pipeline] {
22:04:33  [Pipeline] stage
22:04:33  [Pipeline] { (Print Azure Credentials)
22:04:33  [Pipeline] script
22:04:33  [Pipeline] {
22:04:33  [Pipeline] withCredentials
22:04:33  [Pipeline] // withCredentials
22:04:33  [Pipeline] }
22:04:33  [Pipeline] // script
22:04:33  [Pipeline] }
22:04:33  [Pipeline] // stage
22:04:33  [Pipeline] stage
22:04:33  [Pipeline] { (Declarative: Post Actions)
22:04:33  [Pipeline] sh
22:04:33  + az logout
22:04:33  ERROR: There are no active accounts.
22:04:34  Error when executing always post condition:
22:04:34  Also:   org.jenkinsci.plugins.workflow.actions.ErrorAction$ErrorId: b3ef9e37-7c2d-4d60-8bba-689acf7e0242
22:04:34  hudson.AbortException: script returned exit code 1
22:04:34  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.handleExit(DurableTaskStep.java:668)
22:04:34  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.check(DurableTaskStep.java:614)
22:04:34  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.run(DurableTaskStep.java:555)
22:04:34  	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:539)
22:04:34  	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
22:04:34  	at java.base/java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304)
22:04:34  	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1136)
22:04:34  	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:635)
22:04:34  	at java.base/java.lang.Thread.run(Thread.java:840)
22:04:34  
22:04:34  [Pipeline] }
22:04:34  [Pipeline] // stage
22:04:34  [Pipeline] }
22:04:34  [Pipeline] // node
22:04:34  [Pipeline] End of Pipeline
22:04:34  ERROR: Credentials 'azure' is of type 'Azure Service Principal' where 'com.cloudbees.plugins.credentials.common.StandardUsernamePasswordCredentials' was expected
22:04:34  Finished: FAILURE
