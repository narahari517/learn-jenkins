pipeline {
    agent {
        label 'agent-1'
    }
    options {
        timeout(time: 15, unit: 'SECONDS')
    }
    stages {
        stage('Build') {
            steps {

                    sh "echo This is build"
                    sh 'sleep 10'

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
                    //error "pipeline failed"

            }
        }
    }

    post {
        always{
            echo "This section runs always"
            deleteDir()
        }
        success{
            echo "This section runs when pipeline success"
        }
        failure{
            echo "This section runs when pipeline failure"
        }
    }
}