pipeline {
    agent any

    environment {
        TARGET_DIR = "/home/ubuntu/develop-code"
    }

    stages {

        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Clone Develop Branch') {
            steps {
                echo "Cloning develop branch..."
            }
        }

        stage('Prepare Target Directory') {
            steps {
                sh """
                mkdir -p ${TARGET_DIR}
                rm -rf ${TARGET_DIR}/*
                """
            }
        }

        stage('Copy Files to Target Directory') {
            steps {
                sh """
                cp -r * ${TARGET_DIR}/
                """
            }
        }

        stage('Verification') {
            steps {
                sh "ls -l ${TARGET_DIR}"
            }
        }
    }
}
