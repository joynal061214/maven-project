pipeline {
    agent any

    tools {
        maven 'localMVN'
    }
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
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