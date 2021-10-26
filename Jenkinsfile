pipeline {
    
    agent any

    stages {
        stage('build'){
            steps {
                sh 'deno run --allow-net index.ts'
            }
        }

        stage('publish') {
            docker.withRegistry('https://index.docker.io/v1/', 'dockerhub') {                         //define dockerhub registry and credentials id
                def app = docker.build("aminekader/deno-app:${commit_id}", '.')  //build and push
            }
        }
    }
}