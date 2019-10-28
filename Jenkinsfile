podTemplate(label: 'docker-node', containers: [containerTemplate(name: 'centos', image: 'jenkins/centos-slave:centos8', ttyEnabled: true, command: 'cat')])
    {
node('docker-node') {
    stage('Docker image') {
        container('centos') {
            sh 'cat /etc/redhat-release'
            }
        }
    }
}    