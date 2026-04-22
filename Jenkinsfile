pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                script {
                        sh """
                            echo "Building"
                        """
                }
            }
        }
        stage('Test') { 
            steps {
                script {
                        sh """
                            echo "Testing"
                        """
                }
            }
        }
        stage('Deploy') { 
            steps {
                script {
                        sh """
                            echo "Deploy"
                        """
                }
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
