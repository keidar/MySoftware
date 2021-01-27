pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                script {
                    properties([pipelineTriggers([pollSCM('*/30 * * * *')])])
                }
                git 'https://github.com/keidar/MySoftware.git'
            }
        }
        stage('run python') {
            steps {
                script {
                    sh 'python First_file.py'

                }
            }
        }
    }
}
