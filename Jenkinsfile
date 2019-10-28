def dockerfile = "dockerfile"
podTemplate(label: 'docker-node', containers: [containerTemplate(name: 'centos', image: 'centos8:latest', ttyEnabled: true, command: 'cat')])
    {
node('docker-node') {
    stage('Docker image') {
        container('centos') {
            sh 'cat /etc/redhat-release'
            }
        }
    }
}    