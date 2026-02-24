pipeline {
    agent any

    stages {
        stage('Build React App') {
            steps {
                bat '''
                    echo ===== Checking Versions =====
                    node --version
                    npm --version

                    echo ===== Installing Dependencies =====
                    npm install

                    echo ===== Building Project =====
                    npm run build

                    echo ===== Listing Files =====
                    dir
                '''
            }
        }
    }
}