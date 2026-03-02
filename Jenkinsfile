pipeline {
    agent any

    stages {
        stage('Fetch') {
            steps {
                echo 'Fetching from Repo...'
                git "https://github.com/Ajinkya-07/demo.git"
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the Program...'
                bat "javac first.java"
            }
        }
        
        stage('execute') {
            steps {
                echo 'Executing the Program...'
                bat "java first"
            }
        }
    }
    post{
        success{
            echo 'Pipeline built successfully'
        }
        failure{
            echo 'Pipeline failed'
        }
    }
}
