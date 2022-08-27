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
        
        
    }
}
