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
                sh 'mvn clean install'
            }
        }
        stage('Unit Test'){
            steps{
                echo 'Executing Unit test cases'
            }
        }
        stage('Docker Build'){
            steps{
                sh 'docker build . -t madhu26/springdemo'
                sh 'docker run -d -p 8082:8082 springdemo:latest' 
            }
        }
        /*post {
                 success {
                    echo 'maven build success :'+env.WORKSPACE
                }
            }*/
    }
}
