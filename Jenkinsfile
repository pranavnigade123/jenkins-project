pipeline {
    agent any

    stages {

        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Clone Repo') {
            steps {
                git 'https://github.com/pranavnigade123/jenkins-project.git'
            }
        }

        stage('Deploy Website') {
            steps {
                sh "cp index.html /var/www/html/"
            }
        }

    }
}
