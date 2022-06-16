node {

  stage('Git checkout') {
    checkout scm
  }

  stage('Maven Package') {
    withMaven (
      maven: 'Maven 3.8.5'
    ){
      sh "mvn clean package"
    }
  }

  stage('Docker build') {

    docker.build("quarkus-hello:${env.BUILD_ID}",
                    "-f src/main/docker/Dockerfile.jvm .")
  }

}