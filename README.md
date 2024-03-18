<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>


22:01:44  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
22:01:44  [Pipeline] Start of Pipeline
22:01:44  [Pipeline] node
22:01:44  Running on jonatan in /var/jenkins_home/workspace/prueba-azure
22:01:44  [Pipeline] {
22:01:44  [Pipeline] stage
22:01:44  [Pipeline] { (Print Azure Credentials)
22:01:44  [Pipeline] script
22:01:44  [Pipeline] {
22:01:44  [Pipeline] withCredentials
22:01:44  [Pipeline] // withCredentials
22:01:44  [Pipeline] }
22:01:44  [Pipeline] // script
22:01:44  [Pipeline] }
22:01:44  [Pipeline] // stage
22:01:44  [Pipeline] stage
22:01:44  [Pipeline] { (Declarative: Post Actions)
22:01:44  [Pipeline] sh
22:01:45  + az logout
22:01:45  ERROR: There are no active accounts.
22:01:45  Error when executing always post condition:
22:01:45  Also:   org.jenkinsci.plugins.workflow.actions.ErrorAction$ErrorId: 41ed096a-4818-4ae6-b369-e4f372476217
22:01:45  hudson.AbortException: script returned exit code 1
22:01:45  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.handleExit(DurableTaskStep.java:668)
22:01:45  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.check(DurableTaskStep.java:614)
22:01:45  	at org.jenkinsci.plugins.workflow.steps.durable_task.DurableTaskStep$Execution.run(DurableTaskStep.java:555)
22:01:45  	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:539)
22:01:45  	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
22:01:45  	at java.base/java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304)
22:01:45  	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1136)
22:01:45  	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:635)
22:01:45  	at java.base/java.lang.Thread.run(Thread.java:840)
22:01:45  
22:01:45  [Pipeline] }
22:01:45  [Pipeline] // stage
22:01:45  [Pipeline] }
22:01:45  [Pipeline] // node
22:01:45  [Pipeline] End of Pipeline
22:01:45  ERROR: Could not find credentials entry with ID 'azure-cli-credentials'
22:01:45  Finished: FAILURE
