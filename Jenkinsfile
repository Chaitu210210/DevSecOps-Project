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
               // git branch: 'DEV', credentialsId: 'a9c8653d-a375-4aa5-82e8-835d86405084', url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
         //   git branch: 'UAT', credentialsId: 'a9c8653d-a375-4aa5-82e8-835d86405084', url: 'https://github.com/Chaitu210210/DevSecOps-Project.git'
                 }
        }
        stage('Move Directories') {
            steps {
                script {
                   script {
                    sh 'sudo rm -rf /home/ubuntu/DevSecOps-main/*'
                    sh 'ls -l /home/ubuntu/DevSecOps-main/'
                }
                }
                script {
    sh "sudo ls -l /home/ubuntu/DevSecOps-main/"
    sh "sudo rm -rf /home/ubuntu/DevSecOps-main/*"
    sh "sudo ls -l /home/ubuntu/DevSecOps-main/"
}
                script {
                    // Source directory
                    def sourceDir = "/var/lib/jenkins/workspace/DevSecOps-Project_main"

                    // Destination directory
                    def destDir = "/home/ubuntu/DevSecOps-main"

                    // Copy all files from sourceDir to destDir
                    sh "sudo cp -r ${sourceDir}/* ${destDir}"
                }
            }
        }
    }
}    
