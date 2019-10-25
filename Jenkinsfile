#!/usr/bin/env groovy
// def username = 'Jenkins'

pipeline {
    agent any 
    stages {
        stage('HelloWorld') {
            steps {
                sh 'echo "Hello Mr. World"'
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