pipeline {
    agent any

    stages {
        stage('code clone') {
            steps {
               git branch: 'master', url: 'https://github.com/saikumarbaddapuri10/react_django_demo_app.git'
            }
        }
        stage('build image') {
            steps {
               script{
                   sh "docker build -t ghat ."
               }
            }
        }
        stage('build container') {
            steps {
               script{
                   sh "docker run -dt --name contghat -p 8001:8001 ghat"
               }
            }
        }
    }
}
