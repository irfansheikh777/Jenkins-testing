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
                echo "Configuration changes for Dev"
            //  sh ' envr = $(cat userdata.txt)'
            }
         }

        stage('testing stage ') {
         steps {
             script {
            /* groovylint-disable-next-line NoDef, VariableTypeRequired */
            def props = readProperties file: 'userdata.txt'
            env.envrionments = props.envrionments
             }

             sh "envrironment is $envrionments"
         }
        }
    }
}
