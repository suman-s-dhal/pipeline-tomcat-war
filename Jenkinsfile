
node ['0908002b-74b3-499d-b33a-a96e77de1859']
{
    stage 'Validatio' {
        sh 'mvn validate'
    }
    stage  'Test' {
        sh 'mvn test'
    }
    stage 'Package' {
        sh 'mvn package'
    }
}
