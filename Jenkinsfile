pipeline {
    agent any
    stages {
        stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
             stage('Checkout Repository') {
                 steps {
            git branch: 'main', credentialsId: 'a9c8653d-a375-4aa5-82e8-835d86405084', url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
                git branch: 'DEV', credentialsId: 'a9c8653d-a375-4aa5-82e8-835d86405084', url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
            git branch: 'UAT', credentialsId: 'a9c8653d-a375-4aa5-82e8-835d86405084', url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
                 }
        }
    }
}    
