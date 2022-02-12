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
                bat "npm install"
                bat "npm install react-scripts --save"
                git([url:'https://github.com/Marion9/front_back_jenkins.git', branch:'main'])
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