pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    def srn = PES2UG21CS932 // Replace 12345 with your actual SRN
                    def cppFile = "file${srn - 1}.cpp"
                    sh "g++ ${cppFile} -o output"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished'
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
