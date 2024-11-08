pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                git url: 'https://github.com/username/repository.git', credentialsId: 'github-credentials'
            }
        }

        stage('Build') {
            steps {
                // Commands for building the project
                sh 'echo Building the project...'
            }
        }

        stage('Test') {
            steps {
                // Commands for testing the project
                sh 'echo Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                // Commands for deploying the project
                sh 'echo Deploying the project...'
            }
        }
    }

    post {
        always {
            // Example: archive the artifacts generated
            archiveArtifacts artifacts: '**/target/*.jar', allowEmptyArchive: true
        }
    }
}
