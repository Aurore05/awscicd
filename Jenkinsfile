pipeline {
    agent any

environment {
 BRAIN_NAME = 'main'
 GIT-URL = 'https://github.com/Aurore05/awscicd.git'
}


 stages {
    stage ('git checkout') {
        steps{
            git branch: "${BRANCH_NAME}", url: "{GIT_URL}"
        }
    }
    stage ('docker build'){
        steps {
            sh 'docker build -t awscicd .'
            sh 'docker images'
        }
    }
 }


}