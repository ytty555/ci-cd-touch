pipeline {
    agent any

    tools {
        jdk 'java17'
    }

    stages {
        stage("Start docker daemon") {
            steps {
                sh 'dockerd'
            }
        }

        stage("Verify tooling") {
            steps {
                sh '''
                    docker version
                    docker info
                    docker compose version
                    curl --version
                '''
            }
        }

        stage('Build') {
            steps {
                sh '''
                    ./mvnw clean install -DskipTests -T 1C
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
                sh 'docker compose up -d'
            }
        }
    }
}