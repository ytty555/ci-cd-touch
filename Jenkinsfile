pipeline {
    agent any

    tools {
        jdk 'Java17'
    }

    stages {
        stage('Build') {
            steps {
                sh '''
                    ./mvnw clean install -DtestsSkip=true
                '''
            }
        }

        stage('Test') {
            steps {
                sh './mvnw clean test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploing...'
            }
        }
    }
}