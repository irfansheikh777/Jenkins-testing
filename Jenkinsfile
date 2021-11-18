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
                echo "envr = $envr"
            }
         }

        stage('testing stage ') {
         steps {
               echo 'testing pipe'
         }
        }
    }
}
