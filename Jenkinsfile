pipeline {
    agent any
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