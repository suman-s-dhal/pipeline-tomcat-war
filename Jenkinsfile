pipeline {
    agent { label 'demo-slave' }
    tools {
        maven 'm4'
    }
    stages {
        stage('Build') {
           steps {
              echo "Cleaning the maven project"
              sh 'mvn clean'
           }
        }
        stage('Package') {
           steps {
              echo "Creating the Project package"
              sh 'mvn package'
           }
        }
        stage('Deploy') {
           steps {
              echo "Deploying the Project"
           }
        }
    }
}
