pipeline {
    agent any

    tools {
        jdk 'jdk17'
    }

    stages {
        stage('Initialize') {
            steps {
                sh '''
                    echo 'Initializing...'
                    echo 'PATH = ${PATH}'
                    echo 'M2_HOME = ${M2_HOME}'
                '''
            }
        }

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