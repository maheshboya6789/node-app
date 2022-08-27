pipeline {
    agent any

    stages {
        stage('GitHub Repo') {
            steps {
                git "https://github.com/anilkumarpuli/node-app.git"
            
            }
        }
        
        stage('Maven Build') {
            steps {
                sh "mvn clean install"
            }
        }
        
        
    }
}
