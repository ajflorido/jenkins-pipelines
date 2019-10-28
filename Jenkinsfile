containerTemplate(name: 'centos', image: 'jenkins/centos-slave:centos8')
node {
    stage('Docker image') {
        container('centos') {
            sh 'cat /etc/redhat-release'
        }
    }
}