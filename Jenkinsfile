pipeline {
    agent any

    stages {
        stage('Git Stage') {
            steps {
                git branch: 'main', url: 'https://github.com/22120362/22120362.git' // add git
            }
        }

        stage('Build and Push Docker Image'){
            steps {
                withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
                        sh 'docker build -t 22120362/22120362 .'
                        sh 'docker push 22120362/22120362'
                    }
                }
            }
        }
    } 

