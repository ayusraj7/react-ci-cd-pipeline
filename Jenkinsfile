pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {

        stage('Clean Workspace') {
            steps {
                echo "===== Cleaning Workspace ====="
                cleanWs()
            }
        }

        stage('Checkout Code') {
            steps {
                echo "===== Checking Out Code From Git ====="
                checkout scm
                bat 'echo ===== Files After Checkout ====='
                bat 'dir'
            }
        }

        stage('Build React App') {
            steps {
                bat 'echo ===== Checking Node and NPM Versions ====='
                bat 'node --version'
                bat 'npm --version'

                bat 'echo ===== Installing Dependencies ====='
                bat 'npm install'

                bat 'echo ===== Building React App ====='
                bat 'npm run build'

                bat 'echo ===== Files After Build ====='
                bat 'dir'
            }
        }
    }

    post {
        success {
            echo "===== BUILD SUCCESSFUL ====="
        }
        failure {
            echo "===== BUILD FAILED ====="
        }
    }
}