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

/*pipeline {
    agent { docker { image 'tomcat:8.5.32' } }
    stages {
        stage('build') {
            steps {
                echo "PATH is: $PATH"
            }
        }
    }
}*/

 node
 {
        stage('build') {
               sh "docker build -t rest-hello /Users/satt/Satheesh/cloud/rest-hello"
               echo "Built docker image for rest-hello"
        }
        stage ('Run Application') {
              sh "docker run --rm -d -p 7080:8080 rest-hello"
              echo "Started Tomcat with rest-hello"
        }
        stage ('Test Application') {
              sh "curl localhost:7080/pipeline/HelloPipeLineService/items"
        }
    }

