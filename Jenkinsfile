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
              sshagent(['0908002b-74b3-499d-b33a-a96e77de1859']) {
                  sh 'mvn package'
              }
           }
        }
        stage('Deploy') {
           steps {
              echo "Deploying the Project"
           }
        }
    }
}
