#!/usr/bin/env groovy
def username = 'Jenkins'

pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    } 
    stages {
        stage('Greetings') {
            steps {
                echo "${params.Greeting} World!"
            }
        }
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