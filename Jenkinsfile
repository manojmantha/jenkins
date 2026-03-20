pipeline{
    agent any
    stages{
        stage("Clone the code"){
            steps{
                script {
                    """
                     echo "Clone the code"
                    """
                }
            }
        }
        
        stage("Install the dependiances"){
            steps{
                echo "Install dependiances"
            }
        }

        stage("Scanning the code"){
            steps{
                echo "Scan the code"
            }
        }

        stage("Testing the code") {
            steps{
                echo "Test the code"
            }
        }
        
        stage("Build the Image"){
            steps{
                echo "Build image"
            }
        }
        
        stage("Deploy the Image"){
            steps{
                echo "Deploy image"
            }
        }
    }

    post{
        always {
            echo "I always shows either success or failure"
            deleteDir()
        }
        success{
            echo "I am from success pipeline"
        }
        failure{
            echo "I am from failure pipeline"
        }
    }
}