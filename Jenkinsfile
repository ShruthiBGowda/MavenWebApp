pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ShruthiBGowda/MavenWebApp.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
        stage('Deploy') {
            steps {
                  sh 'mvn clean package'
            }
        }
    }
}
