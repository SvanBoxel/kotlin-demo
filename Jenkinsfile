pipeline {
    agent {
        dockerfile {
            args '-v $HOME/.gradle:/root/.gradle'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh "./gradlew build"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "./gradlew test"
            }
        }
    }
}