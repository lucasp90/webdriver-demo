pipeline {
    agent { 
        dockerfile {
            filename 'Dockerfile'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            dir('/usr/workspace') {
                sh 'python test_script.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
