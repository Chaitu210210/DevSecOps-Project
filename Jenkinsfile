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
                git branch: 'main' , url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
               git branch: 'new' , url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
            }
        }
        stage('moving') {
            steps {
                script {
                    // Your shell script
                    def result = sh(script: 'sh 'mv  /home/ubuntu/project/DevSecOps-Project@script /home/ubuntu/project/.DevSecOps-Project@script'', returnStatus: true)
                    if (result != 0) {
                        error "Shell script failed with exit code ${result}."
                    }
                }
            }
        }
        stage('Hide Files') {
            steps {
                // Move files to a hidden directory
               // sh 'mv  /home/ubuntu/project/DevSecOps-Project@script /home/ubuntu/project/.DevSecOps-Project@script'
                sh 'rm -rf /home/ubuntu/project/DevSecOps-Project@tmp'
            }
        }   
}
}
