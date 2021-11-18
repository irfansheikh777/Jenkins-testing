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
                new File('userdata.txt').withReader('UTF-8') { reader ->
                def line
                while ((line = reader.readLine()) != null) {
                println "${line}"
                }
                }
            }
            }
                }
    }
}
