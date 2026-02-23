pipeline {
    agent any

    options {
        timeout(time: 1, unit: 'SECONDS')
        buildDiscarder(logRotator(numToKeepStr: '3'))
    }
    environment{
        TEMP_ENV="We don't have a break today???"

    }
    stages {
        stage("stage num 1") {
            steps {
                echo "hello world"
                echo "${TEMP_ENV}"
            }
        }

        stage("stage num 2") {
            steps {
                echo "go to success"
            }
        }
          stage('learn credentials') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: '1',
                        usernameVariable: 'USER',
                        passwordVariable: 'PASS'
                    )
                ]) {
                    bat '''
                        echo Deploying as %USER% %PASS%
                    '''
                }
            }
        }

        stage("stage num 3") {
            steps {
                echo "the first build"
            }
        }

        stage("stage num 4") {
            steps {
                echo "checking previous stage..."

            }
        }
        stage("stage num 5") {
            steps {
                echo "the first deploy"
                echo "the first build"
                echo "the test true"
            }
        }
    }
}