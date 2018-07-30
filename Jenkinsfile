/*pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'java -version'
            }
        }
    }
}*/

pipeline {
    agent { docker { image 'node:6.3' } }
    environment {
        PATH=/usr/local/bin:$PATH
    }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}*/
