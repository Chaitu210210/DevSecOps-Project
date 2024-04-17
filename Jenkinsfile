pipeline {
    agent any
    stages {
        stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout from Git') {
            steps {
               git branch ''
                      credentialsId: '71e90cd9-d137-4930-ba0f-392ad4837bcb',
                        url: 'https://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@github.com/Chaitu210210/DevSecOps-Project.git'
            }
        }
}
}
