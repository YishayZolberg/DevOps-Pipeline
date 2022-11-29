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
                    echo "Building...."
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
