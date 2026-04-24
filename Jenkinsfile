pipeline {
    agent any
    parameters {
        // Yeh checkbox banaye ga Jenkins mein
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Check to run tests')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
            }
        }
        stage('Test') {
            // Agar checkbox uncheck hoga toh ye stage skip ho jayegi
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
