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
               echo "PATH is: $PATH"
            }
        }
        stage ('Run Application') {
        try {
          // Start tomcat container here
          sh "docker run -it --rm -p 7080:8080 tomcat:8.0"
        } catch (error) {
        } finally {
          // Stop and remove database container here
          //sh 'docker-compose stop db'
          //sh 'docker-compose rm db'
        }
  }
    }
}
