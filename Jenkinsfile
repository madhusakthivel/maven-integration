pipeline {
    agent any
    tools {
         maven "myMaven"
    }
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/jglick/simple-maven-project-with-tests.git'
                bat "mvn clean package"
            }
            post {
                 success {
                    echo 'maven build success :'+env.WORKSPACE
                }
            }
        }
    }
}
