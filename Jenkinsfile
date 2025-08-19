pipeline {
    agent any

    stages {
        stage('Checkout') {
            when {
                branch 'main'
            }
            steps {
                checkout scm
            }
        }

        stage('Restore') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build --configuration Release'
            }
        }

        stage('Test') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet test --configuration Release --no-build'
            }
        }
    }
}
