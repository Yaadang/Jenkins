pipeline   {

    agent any
    parameters{
        string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod')
    }
    tools{
        maven 'Maven'
    }

    stages {
        stage("build"){

            steps{
                echo "we in da build phase"
            }
        }
        
        stage("test"){
            steps{
                echo "we in da test phase"
            }
        }
        
        stage("deploy"){

            steps{
                echo "we in da deploy phase"
                echo "deploying version ${params.VERSION}"
            }
        }
    }
}
