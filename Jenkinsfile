//def label = "docker-jenkins-${UUID.randomUUID().toString()"}
def label = "docker-jenkins-${UUID.randomUUID().toString()}"

podTemplate(label: label, containers: [containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat')])
    {
node (label) {
    stage('Build') {
      container('maven') {
            sh 'mvn -version'
            sh 'java -jar jenkins-cli.jar -s http://jenkins:8080/ who-am-i'
            }
        }
    }
}    