pipeline {
    agent any 
        stages{
            stage('Run quality checks'){
                when {
                    branch 'main' 
                }
              steps {
                    sh '/var/lib/jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonar/bin/sonar-scanner \
  -Dsonar.projectKey=harsha \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://52.91.104.46:9000 \
  -Dsonar.login=sqp_080fb61707e40fdf861ee5617a453da88b644efd'
            }
        }
        
    }
}
