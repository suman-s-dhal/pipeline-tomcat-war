pipeline {
    agent any
    tools {
        maven 'm2'
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
    post {
        success {
            sh 'sudo cp -rv /var/lib/jenkins/workspace/test-02/target/*.war /opt/tomcat/apache-tomcat-9.0.37/webapps'
        }
    }    
}
