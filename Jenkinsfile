pipeline {
    agent any 
    
    // test comment
    
  

    stages {
        stage('Build') { 
            steps { 
                sshagent(['584ae7f7-9eda-4321-a4d3-da4f4c0ac171']) {
     sh 'ssh -o StrictHostKeyChecking=no jkalra@10.48.116.95 ls'
}
              //  sshagent (credentials: ['devprod (PEM file)']) {
   // sh 'ssh -o StrictHostKeyChecking=no devprod@10.17.62.130 ls'
   // }

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
