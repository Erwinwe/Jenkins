pipeline {
   agent none 

    stages {
        stage('Back-end') {
            agent {
                label 'Docker-agent'
                docker { image 'maven:3-alpine' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                label 'Docker-agent'
                docker { image 'node:14-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
   
}