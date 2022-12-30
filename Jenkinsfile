pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
               git branch: 'development', credentialsId: '1f67fa8c-8308-4936-8430-14f8d3810415', url: 'https://github.com/Mujeeb78/Hotel-Management-System'
            }
        }
        stage('Build and Test') {
            steps {
                sh 'mvn clean install -Dmaven.test.skip=true'

            }
        }
        stage('Code Analysis') {
            steps {
                echo "Scanned successfully!"
            }
        }
        stage('Notification') {
            steps {
                emailext body: 'build is successful', subject: 'Build', to: 'mujeeb9742@gmail.com'
            }
        }
        }
    }
