pipeline {
    agent any

    tools {
        jdk 'Java17'
    }

    stages {
        stage('Build') {
            steps {
                sh '''
                    echo 'Building...'
                    ./mvnw -Dmaven.test.failure.ignore=true install
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploing...'
            }
        }
    }
}