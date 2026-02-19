pipeline {
    agent any

    // Task 2: Define Choice parameter
    parameters {
        choice(
            name: 'ENVIRONMENT', 
            choices: ['DEV', 'TEST', 'PROD'], 
            description: 'Select the target environment for this build.'
        )
    }

    stages {
        stage('Task 1: Checkout') {
            steps {
                // Pulls the updated repository version
                checkout scm
            }
        }

        stage('Task 3: Print Selection') {
            steps {
                // Task 3: Print selected environment in console
                echo "---------------------------------------"
                echo "DEPLOYING TO: ${params.ENVIRONMENT}"
                echo "---------------------------------------"
                
                // Optional: Run the python script to show it exists
                bat 'python verify_env.py'
            }
        }
    }
}