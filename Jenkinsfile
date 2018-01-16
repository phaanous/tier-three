pipeline {
    agent any

    parameters {
        booleanParam(name: 'DO_BUILD', defaultValue: false, description: 'Will be bassed by integration job')
    }

    stages {
        stage('Build') {    

            when { 
                anyOf {
                    environment name: 'FEATURE_BUILD', value: true
                    branch: 'master'
                }
            }

            steps {
                echo 'Building..'
                echo env.BRANCH
                sleep(2) {
                    echo 'Waiting for 2 seconds'
                }
                echo 'Built completed in 2 seconds'
            }        
        }
        
        stage('Test') {

            when { 
                anyOf {
                    environment name: 'FEATURE_BUILD', value: true
                    branch: 'master'
                }
            }

            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {

            when { 
                anyOf {
                    environment name: 'FEATURE_BUILD', value: true
                    branch: 'master'
                }
            }

            steps {
                echo 'Deploying....'
            }
        }
    }
}