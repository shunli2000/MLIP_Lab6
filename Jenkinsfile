pipeline {
    agent any

    stages { 
        stage('Build') {
            steps {
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo Test Step: We run testing tool like pytest here

                REM Initialize conda
                C:\\Users\\shunli\\anaconda3\\Scripts\\activate mlip

                REM Run pytest
                pytest

                echo pytest did not run
                exit 1 REM comment this line after implementing Jenkinsfile
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
