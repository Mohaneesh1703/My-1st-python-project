pipeline {
    agent any

    tools {
        jdk 'JDK11' // Configure this in Jenkins tools
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/<your-username>/<repo-name>.git'
            }
        }

        stage('Build') {
            steps {
                sh 'javac StudentRepository.java'
            }
        }

        stage('Test') {
            steps {
                sh 'java StudentRepository'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*.class', allowEmptyArchive: true
            }
        }
    }
}
