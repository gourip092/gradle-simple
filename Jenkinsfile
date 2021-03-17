pipeline {
    agent any
    tools {
        gradle 'gradle7'
    }
    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/gourip092/gradle-simple.git'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }
    }
}
