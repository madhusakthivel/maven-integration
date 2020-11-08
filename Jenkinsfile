pipeline {
    agent any
    tools {
         maven "myMaven"
    }
    stages {
        stage('Build') {
            steps {
                //git 'https://github.com/madhusakthivel/JenkinsMavenInt.git'
                //bat "mvn clean package"
                git 'https://github.com/madhusakthivel/springboot-demo.git'
                sh "mvn clean package"
            }
        }
        stage('Unit Test'){
            steps{
                echo 'Executing Unit test cases'
            }
        }
        /*post {
                 success {
                    echo 'maven build success :'+env.WORKSPACE
                }
            }*/
    }
}
