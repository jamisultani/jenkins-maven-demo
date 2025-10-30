pipeline {
    agent any
    tools {
        maven 'Maven-3.9.6'
        jdk 'JDK-21'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build & Test') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
    post {
        success {
            echo '✅ Build Success — CI Pipeline Completed!'
        }
        failure {
            echo '❌ Build Failed — Check Console Output.'
        }
    }
}
