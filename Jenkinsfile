@Library('github-org/repo-name@branch') _

pipeline {
    agent any

    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
        choice(name: 'ENVIRONMENT', choices: ['dev', 'test', 'prod'], description: 'Select environment')
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Building branch: ${params.BRANCH_NAME}"
                git branch: "${params.BRANCH_NAME}", 
                     url: 'https://github.com/bolawisa/my-pipeline-project.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building for ${params.ENVIRONMENT}"
                // Add build commands here
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to ${params.ENVIRONMENT}"
                // Add deployment commands here
            }
        }
    }
}