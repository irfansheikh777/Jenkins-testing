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

         stage('Deployment-Ansible ') {
         steps {
             script {
              if (readFile('userdata.txt').contains('dev')) {
              echo 'Running Ansible playbook for development ...'
                   sh "ansible-playbook  -i host.ini  playbook.yml -e target='dev' "
              }
              if (readFile('userdata.txt').contains('stag')) {
                  echo 'Running Ansible playbook for staging ...'
                 sh "ansible-playbook  -i host.ini  playbook.yml -e target='stag' "
              }
              else {
                  echo 'Not revelant output   please check your tag file '
              }
             }
         }
         }
    }
}
