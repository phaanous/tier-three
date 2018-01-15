pipeline {
    agent any

    stages {
        stage('Build') {                        
            steps {
                echo 'Building..'
                sleep(2) {
                    echo 'Waiting for 2 seconds'
                }
                echo 'Built completed in 2 seconds'
            }        
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}