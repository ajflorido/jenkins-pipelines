
podTemplate(containers: [ 
    containerTemplate(label: 'maven-node', name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat'),
    containerTemplate(label: 'python-node', name: 'python', image: 'python:2.7.0', ttyEnabled: true, command: 'cat')
    ]) {
    node ('docker-node') {
        stage('Build-Maven') {
        container('maven') {
            sh 'mvn -version'
            }
    node ('python-node') {
        stage('Python'){
        container('python') {
            sh "python --version"
                    }    
                }
            }           
       }    
    }
}    