pipeline {
    agent any
    environment{
        DOCKER_TAG = getDockerTag()
    }
    stages{
        stage('git clone')
        {
        steps{
            sh'rm -rf node-app'
            sh' git clone https://github.com/anilkumarpuli/node-app.git'
        }
        }
        stage('build'){
            steps{
                sh'mvn clean install'
            }
        }
    }
}
def getDockerTag(){
    def tag  = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}
