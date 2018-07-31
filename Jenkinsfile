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

/*pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}*/

pipeline {
    agent { docker { image 'tomcat:8.0' } }
    stages {
        stage('build') {
            steps {
               bash 'docker images'
            }
        }
    }
}
