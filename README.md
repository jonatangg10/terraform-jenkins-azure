<p align="center">¡ BIENVENIDO !</p>
<p align="center"><b>Ejemplo practico de Terraform, Jenkins y Azure</b></p>
<hr>
<p align="center"><b>¡ Sigue los pasos en el archivo "Pasos a seguir.pdf" !</b></p>
21:58:15  Lanzada por el usuario Jonatan Stiven Gutierrez Nieto
21:58:15  org.codehaus.groovy.control.MultipleCompilationErrorsException: startup failed:
21:58:15  WorkflowScript: 6: Invalid parameter "secret", did you mean "name"? @ line 6, column 92.
21:58:15     nt Secret', defaultValue: '', secret: tr
21:58:15                                   ^
21:58:15  
21:58:15  1 error
21:58:15  
21:58:15  	at org.codehaus.groovy.control.ErrorCollector.failIfErrors(ErrorCollector.java:309)
21:58:15  	at org.codehaus.groovy.control.CompilationUnit.applyToPrimaryClassNodes(CompilationUnit.java:1107)
21:58:15  	at org.codehaus.groovy.control.CompilationUnit.doPhaseOperation(CompilationUnit.java:624)
21:58:15  	at org.codehaus.groovy.control.CompilationUnit.processPhaseOperations(CompilationUnit.java:602)
21:58:15  	at org.codehaus.groovy.control.CompilationUnit.compile(CompilationUnit.java:579)
21:58:15  	at groovy.lang.GroovyClassLoader.doParseClass(GroovyClassLoader.java:323)
21:58:15  	at groovy.lang.GroovyClassLoader.parseClass(GroovyClassLoader.java:293)
21:58:15  	at org.jenkinsci.plugins.scriptsecurity.sandbox.groovy.GroovySandbox$Scope.parse(GroovySandbox.java:163)
21:58:15  	at org.jenkinsci.plugins.workflow.cps.CpsGroovyShell.doParse(CpsGroovyShell.java:190)
21:58:15  	at org.jenkinsci.plugins.workflow.cps.CpsGroovyShell.reparse(CpsGroovyShell.java:175)
21:58:15  	at org.jenkinsci.plugins.workflow.cps.CpsFlowExecution.parseScript(CpsFlowExecution.java:635)
21:58:15  	at org.jenkinsci.plugins.workflow.cps.CpsFlowExecution.start(CpsFlowExecution.java:581)
21:58:15  	at org.jenkinsci.plugins.workflow.job.WorkflowRun.run(WorkflowRun.java:335)
21:58:15  	at hudson.model.ResourceController.execute(ResourceController.java:101)
21:58:15  	at hudson.model.Executor.run(Executor.java:442)
21:58:15  Finished: FAILURE
