pipeline {
    agent any

    options {timestamps()}
    def mvnHome = tool name: 'maven3.9', type: 'maven'

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
            steps {
                sh "${mvnHome}/bin/mvn clean package"
            }          
        }       
    }
}
