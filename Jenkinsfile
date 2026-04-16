pipeline {
    agent any
    stages {
        stage('CheckOut-SCM') {
            steps {
                cleanWs()
                git branch: 'main', credentialsId: 'user-EdenEcole', url: 'https://github.com/EdenEcole/b3depogithub.git'
            }
        }
        stage('Build-image-nginx') {
            steps {
                sh 'docker build -t mon-nginx .'
            }
        }
    }
}
