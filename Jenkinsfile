node('docker') { // I want a slave labeled "Docker" (i.e. with Docker installed)
  docker.image('python:latest').inside { // Let's use the latest Python image
    checkout scm // Run the job normally...

    stage 'test'
    sh 'make test'

    stage 'publish'
    sh 'make publish'
  }
}
