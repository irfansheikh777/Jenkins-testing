/* groovylint-disable DuplicateStringLiteral */
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
                echo 'Configuration changes for Dev'
            }
         }

        stage('testing stage ') {
         steps {
             script {
            /* groovylint-disable-next-line NoDef, VariableTypeRequired */
            def props = readProperties file: 'userdata.txt'
            env.envrionments = props.envrionments
             }
             echo  "envrironment is ${envrionments}"
         }
        }

         stage('testing read file ') {
         steps {
             script {
              if (readFile('userdata.txt').contains('dev')) {
              echo 'present'
              //     sh "ansible-playbook  -i host.ini  playbook.yml -e target="prod"
              }
              if (readFile('userdata.txt').contains('stag')) {
                   echo 'staging environment'
              }
              else {
                  echo 'Not revelant output   please check your tag file '
              }
             }
         }
         }
    }
}
