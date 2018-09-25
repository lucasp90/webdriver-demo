pipeline {
    agent { 
        dockerfile {
            filename 'Dockerfile'
            args '-v $(pwd):/usr/workspace'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                dir('/usr/workspace') {
                    sh 'python test_script.py'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
