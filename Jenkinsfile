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
            when{
                expression{
                    BRANCH_NAME=='multi-branch-triggers'                  
                }
            }    
            steps{
                script{
                    echo "we are deploying from the 2nd branch"
                    gv.deploy()
                }
            }
        }

    }

}
