pipeline {
    agent any

    stages {
        stage('GitHub Repo') {
            steps {
                git "git clone https://github.com/anilkumarpuli/node-app.git"
            }
        }
        
        stage('Maven Build') {
            steps {
                sh "mvn clean install"
            }
        }
        
         stage('Deploy to Tomcat server') {
            steps {
              sshagent(['Deploy-User']) {
                
                   sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/cdk-demo/target/webapp.war ubuntu@35.80.21.34:/opt/tomcat/webapps" 
               }
            }
        }
    }
}
