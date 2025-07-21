pipeline {
    agent any

    tools {
        maven 'Maven 3.6.9'
    }

    stages {
        stage('build') {
            steps {
                echo 'Compiling sysfoo app...'
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                echo 'Running unit tests...'
                sh 'mvn clean test'
            }
        }
        stage('package') {
            steps {
                echo 'Packaging the app...'
                sh 'mvn -DskipTests'
            }
        }
    }

    post {
        always {
            echo 'This pipeline has completed.'
        }
    }
}
