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
            emailext(body: """Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}  is failed . More info at: ${env.BUILD_URL}""", 
 subject: "${status} : Job ${env.JOB_NAME} build ${env.BUILD_NUMBER} ", 
 to: "manasi.panda@mindtree.com")
        }
    }
}
