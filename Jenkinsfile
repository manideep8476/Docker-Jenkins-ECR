node {
  stage 'Checkout'
  git 'https://github.com/manideep8476/docker-pipeline-demo.git'
 
  stage 'Docker build'
  docker.build('manideep8476:latest')
 
  stage 'Docker push'
  docker.withRegistry('https://464375181876.dkr.ecr.us-east-1.amazonaws.com/manideep8476', 'ecr:us-east-1:ECR-credentials') {
    docker.image('manideep8476').push('latest')
  }
}
