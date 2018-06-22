pipeline {
    agent any 
    
    stages {
        stage('Build') { 
            steps { 
                sh 'echo Building the first pipeline. With testing the organization change' 
            }
        }
        stage('Test'){
            steps {
                sh 'echo Testing...'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Final stage deployed....'
            }
        }
    }
}
