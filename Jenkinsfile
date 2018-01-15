pipeline {
    agent any

    stages {
        stage('Build') {                        
            steps {
                echo 'Building..'
                sleep {
                    time: 2
                    unit: seconds
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