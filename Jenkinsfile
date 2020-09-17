pipeline {
    agent any
    tools {
        maven 'm4'
    }
    stages {
        stage('Build') {
           steps {
               sshagent(['slave-jenkins']) {
                    echo "Cleaning the maven project"
                    sh 'mvn clean'
               }
           }
        }
        stage('Package') {
           steps {
               sshagent(['slave-jenkins']) {
                    echo "Cleaning the maven project"
                    sh 'mvn package'
               }
           }    
        }
        stage('Deploy') {
           steps {
               sshagent(['slave-jenkins']) {
                    echo "Deploying the maven project"
               }
           }    
        }
    }
}
