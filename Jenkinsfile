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
        stage("build" jar){

            steps{
               gv.buildJar()
            }
        }
        stage("build image"){

            steps{
                gv.buildimage()
            }
        }
        stage("deploy"){

            steps{
                gv.deploy()
            }
        }

    }

}
