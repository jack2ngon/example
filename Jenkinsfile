pipeline {
    agent any 
    stages {
        stage('building') {
            steps {
                sh 'cp .env.staging .env'
                sh 'composer install'                
            }
        }
        stage('testing') {
            steps {
                sh 'php artisan test' 
            }
        }
        stage('deploying') {
            steps {
                echo 'deploying ...' 
            }
        }
    }
}
