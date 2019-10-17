pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python --version'
            }
        }
        stage('Stage 2 - Run hello world') {
            steps {
                sh 'python hello_world.py'
                archiveArtifacts artifacts: 'dist/test.zip'
            }
        }
    }
}
