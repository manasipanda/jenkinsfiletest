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
            emailext body: 'Failure Email post step test', subject: 'Pipeline Failed'
        }
    }
}
