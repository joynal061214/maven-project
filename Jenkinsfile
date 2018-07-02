pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'clean package'
            }
            post {
                success {
                    echo 'Now Archiving.....'
                    achiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}