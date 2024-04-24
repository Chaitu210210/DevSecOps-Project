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
                    // Replace '/path/to/directory' with the actual path to the directory
                    def directoryPath = "/home/ubuntu/DevSecOps-main"

                    // Use sudo to delete all files in the directory
                    sh "sudo rm -rf ${directoryPath}/*"
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
