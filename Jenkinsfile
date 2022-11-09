pipeline {
    agent any 
    stages {
        stage('building') {
            steps {
                sh 'cp .env.staging .env'
                sh 'composer install'
                sh 'chmod -Rf 777 storage'
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
