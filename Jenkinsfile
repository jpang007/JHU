pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Clone') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
                sh './gradlew build' // or your build command
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test' // or your test command
            }
        }
    }
}
