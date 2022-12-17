pipeline {
    agent any

    stages {
        stage("Verify tooling") {
            steps {
                sh '''
                    docker version
                    docker info
                    docker compose version
                    curl --version
                    jq --version
                '''
            }
        }
    }

//    tools {
//        jdk 'Java17'
//        'org.jenkinsci.plugins.docker.commons.tools.DockerTool' '18.09'
//    }
//
//    stages {
//        stage('Build') {
//            steps {
//                sh '''
//                    ./mvnw clean install -DskipTests -T 1C
//                '''
//            }
//        }
//
//        stage('Test') {
//            steps {
//                sh './mvnw clean test'
//            }
//        }
//
//        stage('Deploy') {
//            steps {
//                sh 'docker compose up -d'
//            }
//        }
//    }
}