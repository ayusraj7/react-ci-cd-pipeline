pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                    node --version
                    ls 
                    npm install
                    npm run build
                    ls
                '''
            }
        }
    }
}