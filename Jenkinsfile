pipeline {
    agent any
    environment{
        name='gautam'
    }
    parameters{
        string(name:'branch',defaultValue:'')
    }
    stages {
        stage('Hello') {
            steps {
                sh 'echo "Hello World"'
            }
        }
        stage('environment variable') {
            environment{
                local_val='hi i am local to this step.'
            }
            steps {
                sh 'echo $BUILD_ID'
                sh 'echo $name'
                sh 'echo $local_val'
            }
        }
        stage('parameters') {
            steps {
                sh 'echo $branch'
                // echo "Success"
            }
        }
        stage('final') {
            steps {
                sh 'echo $name'
                echo "Success"
            }
        }
    }
}
