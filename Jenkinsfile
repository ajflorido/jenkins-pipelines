def dockerfile = "dockerfile"
podTemplate(label: 'docker-node', containers: [containerTemplate(name: 'centos', image: 'jenkins/centos-slave:dockerfile', ttyEnabled: true, command: 'cat')])
    {
node('docker-node') {
    stage('Docker image') {
        container('centos') {
            sh 'cat /etc/redhat-release'
            }
        }
    }
}    