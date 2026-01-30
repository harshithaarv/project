pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Creating zip artifact'
                sh 'zip -r app.zip .'
            }
        }

        stage('Archive') {
            steps {
                echo 'Archiving artifact'
                archiveArtifacts artifacts: 'app.zip'
            }
        }
    }
}
