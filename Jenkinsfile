pipeline {
    agent {
        docker {
            image 'maven:alpine-test'
            label 'dockernode'      
        }
    }
    stages {
        stage('Checkout') {
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
