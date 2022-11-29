pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    environment {
        IMAGE_NAME = "test"
    }
    stages {
        /*stage('pull from private repo') { 
            steps {
                sh 'rm -fr amits-project'
                sh 'git clone https://github.com/YishayZolberg/DevOps-Pipline.git'
            }
        }
        */
        stage('Build jar') { 
            steps {
                    echo "Building jar.."
                    sh 'mvn package'
            } 
        }
        
        stage('create docker image') { 
            steps {
                script {
                    echo "Building docker image.."
                    sh "docker build -t $IMAGE_NAME:1.0 . "
                } 
            }
        }
        stage('Deploy') { 
            steps {
                echo "1" 
            }
        }
        stage('Clean WorkSpace') {
            steps {
                cleanWs()
            }
        }
    }
}
