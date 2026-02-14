pipeline {
    agent any

    stages {

        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        sstage('Clone Repo') {
    steps {
        git branch: 'main', url: 'https://github.com/pranavnigade123/jenkins-project.git'
    }
}
        stage('Deploy Website') {
            steps {
                sh "cp index.html /var/www/html/"
            }
        }

    }
}
