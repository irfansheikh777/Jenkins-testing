pipeline {
    agent {
        label 'mydesktop'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

         stage('Configration-Changes') {
            steps {
                // Configuration changes for Dev
                sh ' envr = $(cat userdata.txt)'
                
            }
         }

        stage('testing stage ') {
         steps {
               script {
                readFile('userdata.txt')
}
         }
        }
        
        
        
    }
}
