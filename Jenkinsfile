pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
				echo "开始构建"
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
				echo "开始Test"
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}