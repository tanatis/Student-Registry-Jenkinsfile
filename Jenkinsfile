pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                withNPM(npmrcConfig: 'my-custom-nprc') {
                    sh 'npm install'
                }
            }
        }
    }
}