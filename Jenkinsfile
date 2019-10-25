#!/usr/bin/env groovy

pipeline {
    agent any
#    docker.image('centos:7)').inside { 
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