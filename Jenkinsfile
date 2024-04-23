pipeline {
    agent any
      options {
        skipDefaultCheckout(true)
    }
    stages {
        stage('Checkout Repository') {
            steps {
                // Checkout Git repository into a specific directory
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                          doGenerateSubmoduleConfigurations: false,
                          extensions: [],
                          submoduleCfg: [],
                          userRemoteConfigs: [[url: 'https://github.com/Chaitu210210/DevSecOps-Project.git']]],
                          workspace: '/home/ubuntu/project')
            }
            
        }
    }
}    
