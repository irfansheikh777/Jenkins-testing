pipeline {
    agent {
        label 'mydesktop'
    }
    stages {
        stage('gitcchekout') {
            steps {
                   checkout scm
            }
        }

                stage('conditions') {
            steps {
            script {

                 sh "
                environment = $(cat userdata.txt}
                echo $environment

                 "
            }
                }
    }
}
                }
    }
}
