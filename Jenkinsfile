
podTemplate(label: 'docker-node', containers: [ 
    containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat')]
    containerTemplate(name: 'python', image: 'python:2.7.0', ttyEnabled: true, command: 'cat')
    ]) {
    node ('docker-node') {
        stage('Build-Maven') {
        container('maven') {
            sh 'mvn -version'
            }
    node ('docker-node') {
        stage('Python'){
        container('python') {
            sh "python --version"
                    }    
                }
            }           
       }    
    }
}    