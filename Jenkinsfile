pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cpp -o working'
                 build job: 'pes1ug20cs315-1', wait: false
                 echo 'Build successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat working.cpp'
                echo 'Test successful'
            }
        }

        stage('Deploy') {
            steps {
               
                ech 'Deploy successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
