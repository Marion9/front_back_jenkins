pipeline {
    agent any
    stages {
        stage('lauching NodeJs app'){
            steps {
                bat "docker-compose up"
            }
        }
        stage('lauching NodeJs app'){
            steps {
                bat "cd frontend"
                bat "npm test"
            }
        }
        stage('Pushing new release on git'){
            steps {
                bat 'git commit -am "new release"'
                bat "git push origin release"
            }
        }
    }
}