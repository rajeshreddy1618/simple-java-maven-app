pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /usr/local/src/apache-maven'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
