pipeline {
    agent any

    options {timestamps()}

    stages {
        stage('PreChecks'){
            parallel {
                stage('Git Verify') {
                     steps {
                        sh 'git --version'
                    }
                }
                stage('Docker Verify') {
                    steps {
                        sh 'docker --version'
                    }         
                }
            }       
        } 
        stage('mvn package') {
            def mvnHome = tool name: 'maven3.9', type: 'maven'
            sh "${mvnHome}/bin/mvn clean package"
        }       
    }
}
