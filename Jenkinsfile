pipeline {
    agent any
    stages {
        stage('Build Docker image'){
            steps {
                bat "docker-compose build"  
            }
        }
       
        stage('Pushing new release on git'){
            steps {
                bat "git config --global user.email 'bartiermarion@gmail.com'"
                bat "git config --global user.name 'Marion9'"
                bat 'git commit -am "new release"'
                bat "git push origin release"
            }
        }
    }
}