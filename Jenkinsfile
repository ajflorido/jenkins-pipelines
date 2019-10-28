def dockerfile = "dockerfile"
podTemplate(label: 'docker-node', containers: [containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', inside: '-v $HOME/.m2:/root/.m2', ttyEnabled: true, command: 'cat')])
    {
node ('docker-node') {
    stage('Build') {
      container('maven') {
            sh 'mvn -version'
            }
        }
    }
}    