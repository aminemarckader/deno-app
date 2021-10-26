pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                sh 'docker-compose up -d'
            }
        }

        // stage('Publish') {
        //     steps{
        //         withDockerRegistry('https://index.docker.io/v1/', 'dockerhub')
        //         {                         
        //             //define dockerhub registry and credentials id
        //             def app = docker.build("aminekader/deno-app", '.')  //build and push
        //         }
        //     }
        // }
    }
}