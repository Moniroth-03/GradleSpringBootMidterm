pipeline {
    agent any // window agent, Jenkins-laravel (other machine)
    environment {
        BOT_TOKEN = "6853243184:AAF2zVn5Q_bWzgjmAERZjLJp-WEVfMczzDA"
        CHAT_ID = "-1002012810646"
    }
    stages {
        stage('Fetch from GitHub') { //build steps
            steps {
                echo 'Fetching for GitHub'
                git branch: 'main', url: 'https://github.com/Moniroth-03/GradleSpringBootMidterm.git'
            }
        }
        stage('Hello'){
            steps{
                echo'Hello Welcome'
            }
        } 
    }
    post{
            success{
                sh '''
                sh 1-success-deploy.sh;\
                '''
            }
            failure{
                sh '''
                sh 2-fail-deploy.sh;\
                '''
            }
    }

}
    