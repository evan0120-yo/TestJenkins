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
                bat 'mvn clean package'
            }
            post{
                success{
                    echo '開始存檔'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
        stage('Deploy'){
            steps{
                echo "Code Deployed..."
                build job: 'TestJenkinsDeploy'
            }
        }
    }
}