pipeline {
    agent any

    tools {nodejs "node_20"}

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Audit') {
            steps {
                sh 'npm audit'
            }
        }

        stage('Tests') {
            steps {
                sh 'npm run test'
            }
        }

        stage('Deploy') {
            steps {
                script{
                    input('Are you sure you want to deploy?')
                }
                echo 'Deploying'
            }
        }
    }
}