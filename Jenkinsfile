pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "pranavnigade/mywebsite:v1"
        CONTAINER_NAME = "mywebsite-container"
    }

    stages {

        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/pranavnigade123/jenkins-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mywebsite:v1 .'
            }
        }

        stage('Login to DockerHub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub-creds',
                usernameVariable: 'DOCKER_USER',
                passwordVariable: 'DOCKER_PASS')]) {
                    sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
                }
            }
        }

        stage('Tag Image') {
            steps {
                sh 'docker tag mywebsite:v1 $DOCKER_IMAGE'
            }
        }

        stage('Push Image') {
            steps {
                sh 'docker push $DOCKER_IMAGE'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop $CONTAINER_NAME || true'
                sh 'docker rm $CONTAINER_NAME || true'
            }
        }

        stage('Pull Latest Image') {
            steps {
                sh 'docker pull $DOCKER_IMAGE'
            }
        }

        stage('Run New Container') {
            steps {
                sh 'docker run -d -p 8082:80 --name $CONTAINER_NAME $DOCKER_IMAGE'
            }
        }
    }
}
