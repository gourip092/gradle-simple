pipeline {
    agent any
    }
    stages {
        stage('Build') {
            steps {
                gradlew('clean', 'build')
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "deploying to prod"
            }
        }
    }
}
