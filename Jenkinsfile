pipeline {
    agent any

    stages {

        stage('Create Folder') {
            steps {
                sh "mkdir -p devops"
            }
        }

        stage('Create File') {
            steps {
                sh "echo 'Hello from Jenkinsfile CI/CD' > devops/info.txt"
            }
        }

        stage('Read File') {
            steps {
                sh "cat devops/info.txt"
            }
        }

    }
}
