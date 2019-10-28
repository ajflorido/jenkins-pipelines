//def label = "docker-jenkins-${UUID.randomUUID().toString()"}

podTemplate(label: 'docker-node', containers: [containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat')])
    {
node ('docker-node') {
    stage('Build') {
      container('maven') {
            sh 'mvn -version'
            }
        }
    }
}    