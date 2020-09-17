node {
    tools {
        maven 'm4'
    }
    stage('Do something with git') {
        sshagent(credentials: ['demo-slave']) {
            //disply the message
            sh 'mvn clean'
        }
    }
}
