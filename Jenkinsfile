pipeline {
    options{
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
        }

    agent {label 'jenkins-slave-01'}

    tools{
        maven 'maven_3.5.2'
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