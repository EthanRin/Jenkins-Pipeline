pipeline{
    agent any

    environment{
        DIRECTORY_PATH = "Deakin/223/5.1P"
        TESTING_ENVIRONMENT = "testing-space"
        PRODUCTION_ENVIRONMENT = "Sovanpanha-Rin"
    }

    stages{
        stage('Build'){
            steps{
                echo "fetching the source code from $DIRECTORY_PATH"
                echo "compling code and generating necessary artifacts"
            }
        }
        stage('Test'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage('Code'){
            steps{
                echo "checking quality of the code"
            }
        }
        stage('Deploy'){
            steps{
                echo "deploying the application to $TESTING_ENVIRONMENT"
            }
        }
        stage('Approval'){
            steps{
                sleep(time: 10, unit: 'SECONDS')
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "deploying the code to $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}
