pipeline {
    agent any
    environment {
        COURSE = "Jenkins"
    } 
    options {
        timeout(time: 10, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') { 
            steps {
                script {
                        sh """
                            echo "Building"
                            echo $COURSE
                            #sleep 10
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
