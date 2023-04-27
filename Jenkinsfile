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
                    buildApp()
                }
            }
        }
        stage("build image"){

            steps{
                script{
                    buildimage "yaadang/myrepo:jmv-v3"
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
