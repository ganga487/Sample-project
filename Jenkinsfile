pipeline {
    agent {
        docker {
            image 'maven:alpine-test'
            label 'dockernode'      
        }
    }
    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
