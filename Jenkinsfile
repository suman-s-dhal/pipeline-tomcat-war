node {
    stage('Do something with git') {
       sshagent(['0908002b-74b3-499d-b33a-a96e77de1859']) {
          // some block
          sh 'mvn package'
          sh 'cp -rvp /var/lib/jenkins/workspace/pipeline-master /root'
       }
    }
}
