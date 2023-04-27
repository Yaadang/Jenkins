@Library('jenkins-shared-library')
def gv
pipeline   {
    agent any
    tools{
        maven 'maven-3.6'
    }
    stages {
        stage("init"){
            steps{
                script{
                    gv = load "script.groovy"
                }
            }
        }
        stage("build"){

            steps{
                script{ 
                    buildApp("yaadang/myrepo:jmv-v3")
                }
            }
        }
        stage("build image"){

            steps{
                script{
                    buildimage()
                }
            }
        }
        stage("deploy"){

            steps{
                script{
                    gv.deploy()
                }
            }
        }

    }

}
