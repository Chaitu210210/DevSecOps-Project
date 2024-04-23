pipeline {
    agent any
      options {
        skipDefaultCheckout(true)
    }
    stages {
        stage('Checkout Repository') {
            steps {
                    dir('/home/ubuntu/project') {
                git branch: 'main', url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
                }
            } 
            
        }
    }
}    
