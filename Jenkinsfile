
node ['root]']
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
