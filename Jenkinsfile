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
                sh '${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=harsha -Dsonar.sources=. -Dsonar.host.url=:http://52.91.104.46:9000'
             }
         }
     }
}
}

