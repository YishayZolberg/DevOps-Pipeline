pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('pull from private repo') { 
            steps {
                sh 'rm -fr amits-project'
                sh 'git clone https://github.com/YishayZolberg/DevOps-Pipline.git'
            }
        }
        stage('Build jar') { 
            steps {
                script {
                    echo "Building jar.."
                    sh 'mvn package'
                } 
            }
        }
        stage('create docker image') { 
            steps {
                script {
                    echo "Building docker image.."
                    sh 'mvn package'
                } 
            }
        }
        stage('Deploy') { 
            steps {
                echo "1" 
            }
        }
    }
}
