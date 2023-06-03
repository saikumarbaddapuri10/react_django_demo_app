pipeline {
    agent any

    stages {
        stage('code clone') {
            steps {
               git branch: 'master', credentialsId: '7a209082-6d25-48ff-ac02-12895a741803', url: 'https://github.com/saikumarbaddapuri10/react_django_demo_app.git'
            }
        }
        stage('build image') {
            steps {
               script{
                   sh "docker build -t qwerty ."
               }
            }
        }
        stage('build container') {
            steps {
               script{
                   sh "docker run -dt --name cont -p 8002:8001 qwerty"
               }
            }
        } 
        
    }
}
