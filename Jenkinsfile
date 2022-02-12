pipeline {
    agent any
    stages {
        stage('Build NodeJs app'){
            steps {
                bat "docker-compose build"  
            }
        }
        stage('Running test'){
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