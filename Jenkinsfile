pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Placeholder for build steps
                def srn = YOUR_SRN // Replace YOUR_SRN with your actual SRN
                def cppFile = "file${srn - 1}.cpp"
                echo 'Building...'
                sh 'echo "#include <iostream>\n\nint main() {\n    std::cout << \"Hello, World!\" << std::endl;\n    return 0;\n}" > hello.cpp'
            }
        }
        stage('Test') {
            steps {
                // Placeholder for test steps
                echo 'Testing...'
                sh 'g++ hello.cpp -o hello'
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                // Placeholder for deploy steps
                echo 'Deploying...'
                sh 'git add hello.cpp'
                sh 'git commit -m "Add hello.cpp"'
                sh 'git push origin main'
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
