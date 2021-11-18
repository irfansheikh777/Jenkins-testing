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
                sh ' cat userdata.txt'
            }
         }

        stage('testing stage ') {
         steps {
               echo 'testing pipe'
         }
        }
    }
}
