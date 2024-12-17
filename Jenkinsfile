pipeline {
    agent any
    stages {
        stage('Build') {
            steps {

                    sh "echo This is build"

            }
        }
        stage('Test') {
            steps {

                    sh " echo This is TEST"

            }
        }
        stage('Deploy') {
            steps {

                    sh "echo This is deploy"
                    error "pipeline failed"

            }
        }
    }

    post {
        always{
            echo "This section runs always"
        }
        success{
            echo "This section runs when pipeline success"
        }
        failure{
            echo "This section runs when pipeline failure"
        }
    }
}