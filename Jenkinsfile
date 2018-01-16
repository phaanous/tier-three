pipeline {
    agent any

    parameters {
        booleanParam(name: 'FEATURE_BUILD', defaultValue: false, description: 'Will be passed by integration job to indicate it is a feature build')
        string(name: 'BRANCH_TO_BUILD', defaultValue: 'develop', description: 'The target branch')
    }

    stages {

        stage('Build Tier Three') {

            when { 
                anyOf {
                    environment name: 'FEATURE_BUILD', value: 'true';
                    branch 'master'
                }
            }

            steps {                
                echo 'Building..'
                echo env.BRANCH_NAME
                sleep(5) {
                    echo 'Waiting for 2 seconds'
                }
                echo 'Built completed in 2 seconds'
            }        
        }

        stage('Test') {

            when { 
                anyOf {
                    environment name: 'FEATURE_BUILD', value: 'true';
                    branch 'master'
                }
            }

            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {

            when { 
                anyOf {
                    environment name: 'FEATURE_BUILD', value: 'true';
                    branch 'master'
                }
            }

            steps {
                echo 'Deploying....'
            }
        }
    }
}