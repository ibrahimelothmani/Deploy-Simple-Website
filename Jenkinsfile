pipeline {
     agent any
     stages {
          stage('Checkout') {
              steps {
                  git 'https://github.com/ibrahimelothmani/Deploy-Simple-Website.git'
              }
          }
          stage('Build Docker Image') {
              steps {
                  script {
                      docker.build("simple-app:${env.BUILD_NUMBER}")
                  }
              }
          }

          stage('Deploy') {
               steps {
                    // Stop and remove any existing container
                    script {
                         sh "docker stop simple-app || true"
                         sh "docker rm simple-app || true"

                         // Run the new container
                         sh "docker run -d -p 8081:80 --name simple-app simple-app:${env.BUILD_NUMBER}"
                    }
               }
          }
     }
}
