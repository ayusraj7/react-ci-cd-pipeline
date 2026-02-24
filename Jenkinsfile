pipeline {
    agent any

    stages {
        stage('Build React App') {
            steps {
                step('clean up workspace') {
                    cleanWs()
                }

                step('Build Project') {
                  bat 'echo ===== Checking Versions ====='
                bat 'node --version'
                bat 'npm --version'

                bat 'echo ===== Installing Dependencies ====='
                bat 'npm install'

                bat 'echo ===== Building Project ====='
                bat 'npm run build'

                bat 'echo ===== Listing Files ====='
                bat 'dir'
                }
            }
        }
    }
}