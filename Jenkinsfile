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

//pipeline {
    //agent { docker { image 'tomcat:8.0' } }
 node
 {
        stage('build') {
               echo "PATH is: $PATH"
        }
        stage ('Run Application') {
              sh "docker run --rm -p 7080:8080 tomcat:8.0"
        }
    }
//}
