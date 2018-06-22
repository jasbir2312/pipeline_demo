pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
               checkout changelog: false, poll: true, scm: [$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/jasbir2312/demo.git']]]
            }
        }
        stage('Build') { 
            steps { 
                sh 'echo Building Code'
                sh './mvnw clean install -DskipTests=true'    
            }
        }
        stage('Test'){
            steps {
                sh 'echo Executing test cases for the source...'
                sh './mvnw clean install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Final stage deployed....'
            }
        }
    }
}
