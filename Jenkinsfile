#!/usr/bin/groovy
import groovy.json.JsonOutput

pipeline {
    agent { 
                label 'pwalias'
            }

    stages {
        stage('Build') {
            steps {
                sh '''
                    npm i
                    npx playwright test
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
