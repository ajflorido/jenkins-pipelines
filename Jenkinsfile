#!/usr/bin/env groovy
def username = 'Jenkins'

pipeline {
    agent any 
    stages {
        stage('HelloWorld') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                sh 'echo "Hello Mr. ${Jenkins}"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Build"'
                }
            }
        }
    
}