pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Building"
            }
        }
        stage('Test') { 
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploying"
            }
        }
    }
    post {
        always {
            echo "Always running"
            cleanWs()
        }
        success {
            echo "if success it runs"
        }
        failure {
            echo "if fails it runs"
        }
    }
}
