pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                echo "Compiling PES1UG22CS698.cpp"
                g++ PES1UG22CS698.cpp -o PES1UG22CS698
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Running the compiled program"
                ./PES1UG22CS698
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment step (Modify as needed)"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
