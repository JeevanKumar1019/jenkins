pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/JeevanKumar1019/jenkins.git'
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
