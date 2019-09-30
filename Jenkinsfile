pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                eccho 'Hello World'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            mail to: 'manasi.panda@mindtree.com', subject: 'The Pipeline failed :('
        }
    }
}
