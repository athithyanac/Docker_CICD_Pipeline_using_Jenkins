pipeline {
    agent any

    options {timestamp()}

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
    }
}
