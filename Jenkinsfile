pipeline{
    agent {
        label 'AGENT-1'
    }
    environment { 
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 30, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
    stages{
        stage("Clone the code"){
            steps{
                script {
                    echo "Clone the code"
                }
            }
        }
        
        stage("Install the dependiances"){
            steps{
                script{
                    echo "Install dependiances"
                }
            }
        }

        stage("Scanning the code"){
            steps{
                script{
                    echo "Scan the code"
                }
            }
        }

        stage("Testing the code") {
            steps{
                script{
                    echo "Test the code"
                }
            }
        }
        
        stage("Build the Image"){
            steps{
                script{
                    echo "Build image"
                }
            }
        }
        
        stage("Deploy the Image"){
            steps{
                script{
                    echo "Deploy image"
                }
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