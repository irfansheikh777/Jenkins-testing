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
                echo " Configuration changes for Dev"
              //  sh ' envr = $(cat userdata.txt)'
                
            }
         }

        stage('testing stage ') {
         steps {
                environ=$(cat userdata.txt)
         }
        }
        
        
        
    }
}
