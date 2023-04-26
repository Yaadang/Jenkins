pipeline   {

    agent any
    tools{
        maven 'maven-3.6'
    }
    stages {
        stage("build"){

            steps{
                echo "building the application"
                sh 'mvn package'
            }
        }
        stage("build image"){

            steps{
                echo "building the docker image"
                withCredentials([usernamePassword(credentialsId: 'ba245a61-f0b0-4e98-abaa-07a439f7b470',passwordVariable:'PAS',usernameVariable:'USER')]){
                    sh 'docker build -t yaadang/myrepo:jma-2.0 .'
                    sh "echo $PAS | docker login -u $USER --password-stdin "
                    sh 'docker push yaadang/myrepo:jma-2.0'
                }
            }
        }
        stage("deploy"){

            steps{
                echo "deploying the application"
            }
        }

    }
}
