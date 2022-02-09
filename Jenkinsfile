pipeline {
    agent any
    stages {
        stage('lauching NodeJs app'){
            steps {
                bat "echo lauching NodeJs app"
                bat "docker-compose up"
            }
        }
        stage('Creating file and pushing on git'){
            steps {
                bat "echo creating file"
                bat "echo this is a release > release.txt"
                bat 'git commit -am "release"'
                bat "git push origin release"
            }
        }
    }
}