pipeline {
    agent any

    stages {

        stage('Build Image') {
            steps {
                sh 'docker build -t devops-demo:latest .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker rm -f devops-demo || true'
                sh 'docker run -d --name devops-demo -p 8081:80 devops-demo:latest'
            }
        }
    }
}
