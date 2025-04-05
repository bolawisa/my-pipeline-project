pipeline {
    agent any

    parameters {
        // String parameter to choose the branch name
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
        
        // Choice parameter to select the environment (dev/test/prod)
        choice(name: 'ENVIRONMENT', choices: ['dev', 'test', 'prod'], description: 'Select the environment')
    }

    stages {
        stage('Checkout') {
            steps {
                // Using BRANCH_NAME parameter to checkout the branch
                echo "Checking out branch ${params.BRANCH_NAME}"
                git branch: "${params.BRANCH_NAME}", url: 'https://github.com/bolawisa/my-pipeline-project.git'
            }
        }
        stage('Build') {
            steps {
                // Using ENVIRONMENT parameter to specify the environment
                echo "Building for environment: ${params.ENVIRONMENT}"
                echo 'Building the project...'
            }
        }
        stage('Deploy') {
            steps {
                // Using ENVIRONMENT parameter to specify the deployment environment
                echo "Deploying to ${params.ENVIRONMENT} environment"
                echo 'Deploying the project...'
            }
        }
    }
}
