pipeline {
    agent any

    stages {
        stage('Git Verify') {
            steps {
                git branch: 'dev', credentialsId: 'github', url: 'https://github.com/athithyanac/Docker_CICD_Pipeline_using_Jenkins.git'
            }
        }
        stage('mvn package') {
                    def mvnHome = tool name: 'maven', type: 'maven'
                    def mvnCMD = "${mvnHome}/bin/mvn"
                    sh "${mvnCMD} clean package"
                }             
    }
}
