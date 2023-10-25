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
                    npx playwright install
                    npx playwright test
                '''
            }
        }
        
       post{
           always {
               archiveArtifacts artifacts: 'playwright-report/index.html', followSymlinks: false
           }
       }
    }
}
