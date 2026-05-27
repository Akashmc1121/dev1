pipeline {

    agent any

    stages {

 
        stage('Build') {
            steps {
                echo 'Building Application'
            }
        }

   
        stage('Test') {
            steps {
                echo 'Running Test Cases'
            }
        }

    
        stage('Deploy') {
            steps {
                echo 'Deploying Application'
            }
        }
    }

    post {

        success {
            echo 'Pipeline Success'
        }

        failure {
            echo 'Pipeline Failed'
        }

        always {
            echo 'Pipeline Completed'
        }
    }
}
