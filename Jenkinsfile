pipeline {
    agent any

    stages {
        stage('Checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '5f9dbbaf-c93a-4c93-965c-bfbb690551a6', url: 'https://github.com/adharsh-18/simplejava.git']])
            }
        }
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', credentialsId: '5f9dbbaf-c93a-4c93-965c-bfbb690551a6', url: 'https://github.com/adharsh-18/simplejava.git'

            }

            
        }
        stage('Run'){
            steps{
                bat 'java test.java'
            }
        }
    }
    
}
