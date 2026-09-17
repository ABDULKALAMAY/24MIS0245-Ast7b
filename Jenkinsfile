pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ABDULKALAMAY/24MIS0245-Ast7b.git'
            }
        }
 
        stage('Generate Report') {
            steps {
                bat 'python app.py'
            }
        }
 
        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
