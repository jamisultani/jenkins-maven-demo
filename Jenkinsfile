pipeline {
    agent any
    tools {
        maven 'MAVEN-3.8.7'  // Terminal aur Jenkins me jo Maven hai
        jdk 'JDK-21'         // Terminal aur Jenkins me jo JDK hai
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
