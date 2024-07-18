pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    options {
        timeout(time: 1, unit: 'HOURS')
    }
    //#Built
    stages {
        stage( 'Build' ){
            steps {
                echo 'Building...'
            }

        }
        stage( 'Test' ){
            steps {
                echo 'Testing'
            }
        }
        stage( 'Deploy' ){
            steps {
                sh """

                echo "Here I wrote Shell Script"

                """
            }
        }
    }

    //#Post Build
    post {
        always {
            echo 'I will always say Hello Again'
        }
        failure {
            echo 'this runs when pipeline is failed used generally to send some alerts'
        }
        success {
            echo 'I will say hello when pipeline is success'
        }
    }
}