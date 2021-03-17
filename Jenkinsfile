pipeline {
    agent any
    }
    stages {
        stage('Build') {
            steps {
                gradlew('clean', 'build')
            }
        }
        stage('Promotion') {
            steps {
                timeout(time: 1, unit:'DAYS') {
                    input 'Deploy to Production?'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "deploying to prod"
            }
            post {
                failure {
                    mail to: 'gourip092@gmail.com', subject: 'Build failed', body: 'Please fix!'
                }
            }
        }
    }
}
