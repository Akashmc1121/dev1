pipeline {

    agent any

    tools {
        maven 'Maven'
    }

    environment {
        APP_NAME = "java-maven-app"
        DOCKER_IMAGE = "myapp:v1"
    }

    stages {

       
        stage('Echo Stage') {
            steps {
                echo 'Pipeline Started'
                echo 'Learning Jenkins Declarative Pipeline'
            }
        }

   
        stage('Git Clone') {
            steps {
                git 'https://github.com/jenkins-docs/simple-java-maven-app.git'
            }
        }

    
        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test Stage') {
            steps {
                sh 'mvn test'
            }
        }

       
    post {

        success {
            echo 'Pipeline Executed Successfully'
        }

        failure {
            echo 'Pipeline Failed'
        }

        always {
            echo 'Pipeline Execution Completed'
        }
    }
}
