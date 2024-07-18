pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
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
                echo 'Deploying...'
            }
        }
    }

    //#Post Build
    Post {
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