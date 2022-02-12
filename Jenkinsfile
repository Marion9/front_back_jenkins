pipeline {
    agent any
    stages {
        stage('Build Docker image'){
            steps {
                bat "docker-compose build"  
            }
        }
        stage('Running test'){
            steps {
                bat "npm install jest"
                bat "npm test --prefix ./frontend/"
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