pipeline {
    agent any
    
    // Yahan hum Environment Variables define karte hain
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
                // Environment variable ko use karne ke liye ${env.NAME} likhte hain
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
