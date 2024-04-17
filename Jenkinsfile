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
      stage('deleting') {
          steps {
              script {
                    cp -R /home/ubuntu/project/DevSecOps-Project@script /home/ubuntu/project/.New/DevSecOps-Project@script 
                         rm -R /home/ubuntu/project/DevSecOps-Project@script
                     rm -R /home/ubuntu/project/DevSecOps-Project@tmp
                     }
                 }   
        }
        }
     }
