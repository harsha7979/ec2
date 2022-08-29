pipeline {

agent any

stages{

     stage('Run quality checks') {
         when {
             branch 'main'
         }
         environment {
             scannerHome = tool 'sonar'
         }
         steps {
             withSonarQubeEnv('sonar') {
                sh '${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=harsha -Dsonar.sources=. -Dsonar.host.url=:http://http://18.212.58.20:9000'
             }
         }
     }
}
}
