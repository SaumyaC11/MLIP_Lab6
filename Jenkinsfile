pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                bat '''
                echo 'Test Step: We run testing tool like pytest here'

                REM TODO fill out the path to conda here
                REM sudo /PATH/TO/CONDA init
                call .venv/bin/activate

                REM TODO Complete the command to run pytest
                REM sudo /PATH/TO/CONDA run -n <Envinronment Name> <Command you want to run>
                pytest tests/ --junitxml=report.xml

                echo 'Test Completed'
                REM echo 'pytest not runned'
                REM exit 1 #comment this line after implementing Jenkinsfile
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
