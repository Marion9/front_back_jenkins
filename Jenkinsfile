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
                bat "npm install react-scripts --save"
                git([url:'https://github.com/Marion9/front_back_jenkins.git', branch:'main'])
                dir('frontend') {
                    bat "cd"
                }
                bat "dir"
                //bat "npm test --prefix ./frontend/"
            }
        }
        stage('Pushing new release on git'){
            steps {
                bat "git config --global user.email 'bartiermarion@gmail.com'"
                bat "git config --global user.name 'Marion9'"
                bat 'git add .'
                bat 'git commit -m "new release"'
                bat "git push origin release"
            }
        }
    }
}