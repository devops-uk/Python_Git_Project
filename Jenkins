pipeline {
    agent any

    tools {
        maven 'Mymaven'
    }

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/devops-uk/DevOpsCodeDemo.git'
            }
        }

        stage('Compile Code') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Code Review') {
            steps {
                sh 'mvn pmd:pmd'
            }
        }

        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package Code') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
