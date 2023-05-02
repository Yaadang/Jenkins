#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                script {
                    echo "Testing the application..."
                }
            }
        }
        stage('build') {
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }
        stage('deploy') {
            steps {
                script {
                    echo "Deploying the application..."
                    def dockerCmd= "docker-compose -f docker-compose.yaml up --detach"
                    //def dockerCmd= 'docker run -d -p 3080:3080 yaadang/myrepo:reactapp'
                    sshagent(['ec2-server-key']) {
                      sh "scp docker-compose.yaml ec2-user@54.69.133.74:/home/ec2-user"
                      sh "ssh -o StrictHostKeyChecking=no ec2-user@54.69.133.74 ${dockerCmd}"
                    }
                }
            }
        }
    }
}
