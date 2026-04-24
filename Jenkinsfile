pipeline {
    agent any
    
    environment {
        STUDENT_NAME = "Areeba Akmal"
        LAB_NUMBER = "12"
    }
    
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Check to run tests')
    }
    
    stages {
        stage('Build') {
            steps {
           
                echo "Starting Lab ${env.LAB_NUMBER} for ${env.STUDENT_NAME}"
                echo 'Building Project...'
            }
        }
        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing Project...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project...'
            }
        }
    }
}
