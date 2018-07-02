pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean packagepipe'
            }
            post {
                success {
                    echo 'Now Archiving.....'
                    achiveartifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}