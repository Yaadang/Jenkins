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
                    gv.buildApp()
                }
            }
        }
        stage("build image"){

            steps{
                script{
                    gv.buildimage()
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
