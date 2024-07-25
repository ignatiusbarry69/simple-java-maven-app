node {
    docker.image('maven:3.8.5-openjdk-17').inside('-p 3001:3000') {

        dir('/var/jenkins_home/workspace/submission-cicd-pipeline-but-java-Ignatius Barry') {

            stage('Build') {
                echo 'Building the project...'
                sh 'mvn clean compile -X'
            }

            stage('Test') {
                echo 'Running tests...'
                sh 'mvn test -X'
            }
        }
    }
}
