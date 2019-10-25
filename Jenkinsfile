#!/usr/bin/env groovy

pipeline {  
    agent any
    stages {
        stage('HelloWorld') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('Build') {
            steps {
                sh 'ls -la'
            }
        }
    }
}