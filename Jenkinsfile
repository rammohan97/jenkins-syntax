pipeline {
    agent any
    environment {
        COURSE = "Jenkins"
    } 
    options {
        timeout(time: 10, unit: 'SECONDS')
    }
    stages {
        stage('Build') { 
            steps {
                script {
                        sh """
                            echo "Building"
                            echo $COURSE
                            sleep 10
                            env
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
        aborted {
            echo "aborted"
        }
    }
}
