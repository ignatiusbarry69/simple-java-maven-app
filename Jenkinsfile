node {
    checkout scm

    docker.image('maven:3.9.4-eclipse-temurin-17').inside('-p 3000:3000') {

        stage('Build') {
            echo 'Building the project...'
            sh 'mvn clean compile'
        }

        stage('Test') {
            echo 'Running tests...'
            sh 'mvn test'
        }
        stage('Deliver') {
            echo 'Delivering the project...'
            sh 'chmod +x jenkins/scripts/deliver.sh'
            sh './jenkins/scripts/deliver.sh'
        }
    }
}
