pipeline{
    agent {
        label 'AGENT-1'
    }

    // Pre-Build
    environment { 
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 30, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password') 
    }

    // Build
    stages{
        stage("Clone the code"){
            steps{
                script {
                    sh """
                        echo "Hello Clone the code"
                        env
                        echo "I am ${params.PERSON}"
                    """
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

    // Post-build
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