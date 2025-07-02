pipeline {
    agent any

    tools {
        nodejs "NodeJS 18"
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/yourusername/node-ci-sample.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        always {
            echo 'Build Finished!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}
