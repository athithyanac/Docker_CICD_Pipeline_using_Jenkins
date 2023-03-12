pipeline {
    agent any

    stages {
        stage('Git Verify') {
            steps {
                git branch: 'dev', credentialsId: 'github', url: 'https://github.com/athithyanac/Docker_CICD_Pipeline_using_Jenkins.git'
            }
        }
        stage('mvn package') {
            steps {
                def mvnHome = tool name: 'maven', type: 'maven'
                echo($"mvnHome")
            }
        }
    }
}
