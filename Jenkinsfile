pipeline {
    agent any
    stages {
        stage('init'){
            steps{
                echo "Testing..."
            }
        }
        stage('Build'){
            steps{
                echo "Building..."
                sh 'mvn clean package'
            }
        }
        stage('Deploy'){
            steps{
                echo "Code Deployed..."
            }
        }
    }
}