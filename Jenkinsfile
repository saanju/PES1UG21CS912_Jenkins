pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {

                    build 'PES1UG21CS912-1'
                    sh 'g++ hello.cpp -o output'
                
            }
        }
        stage('Test') {
            steps {
               
                    sh './nonexistent'
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure{
             error 'Pipeline failed'
         }
    }
}
