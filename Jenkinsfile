pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/<your-username>/<your-repo-name>.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt || true'
            }
        }

        stage('Run Python Script') {
            steps {
                sh 'python student_repository.py'
            }
        }

        stage('Archive Output') {
            steps {
                archiveArtifacts artifacts: '**/*.txt', allowEmptyArchive: true
            }
        }
    }
}
