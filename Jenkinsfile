
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting the build process...'
                // Add your build commands here, for example:
                // sh 'make build'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here, for example:
                // sh './run_tests.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment commands here, for example:
                // sh 'kubectl apply -f deployment.yaml'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up workspace...'
            cleanWs()
        }
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build or deployment failed.'
        }
    }
}
