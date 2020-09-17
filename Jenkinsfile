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
              sh ' cp -rv /root/workspace/pipeline-master/target/*.war /opt/tomcat/apache-tomcat-9.0.38/webapps'
           }
        }
    }
}
