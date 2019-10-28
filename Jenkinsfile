def dockerfile = "dockerfile"
podTemplate(label: 'docker-node', containers: [containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat')])
    {
node ('docker-node') {
    docker.image.inside('-v $HOME/.m2:/root/.m2')
    stage('Build') {
      container('maven') {
            sh 'mvn -B'
            }
        }
    }
}    