pipeline {
    options{
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
        }

    agent any

    tools{
        maven 'maven_3.8.8'
    }

    stages {
        stage('Code Compilation') {
            steps {
                echo 'code compilation is string'
                sh 'mvn clean compile'
                echo 'code compilation is complete'
            }
        }
        stage('Code Test') {
            steps {
                echo 'code test is starting'
                sh 'mvn clean test'
                echo 'code testing is complete'
            }
        }
        stage('code package') {
            steps {
                echo 'code packaging is starting'
                sh 'mvn clean package'
                echo 'code packaging is completed'
            }
        }
    }
}