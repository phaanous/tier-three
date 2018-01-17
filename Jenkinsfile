pipeline {
    agent any

    stages {        

        stage('Build Tier Three') {

            when { branch 'master' }

            steps {
                echo 'Building..'
                sleep(3) {
                    echo 'Waiting for 3 seconds'
                }
                echo 'Built completed in 3 seconds'
            }        

        }

        stage('Test') {

            when { branch 'master' }

            steps {
                echo 'Testing..'
            }

        }

        stage('Deploy') {

            when { branch 'master' }

            steps {
                echo 'Deploying....'
            }

        }

    }

}