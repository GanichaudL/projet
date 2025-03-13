pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'mkdir -p build'
                dir('build') {
                    sh 'cmake ..'
                    sh 'make'
                }
            }
        }
        stage('Test') {
            steps {
                dir('build') {
                    sh './monprogramme'
                }
            }
        }
    }
}

