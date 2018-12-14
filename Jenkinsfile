node('linux') {
  stage('Create') {
    git credentialsId: 'd33c67f2-739d-4210-82d1-ce3c2c0a4e5d', url: 'https://github.com/wsl100624/jenkinsTest.git'
    
    sh 'aws cloudformation create-stack --stack-name final_test --template-body file://./docker-single-server.json --region us-east-1 --parameters ParameterKey=KeyName,ParameterValue=seis665 ParameterKey=YourIp,ParameterValue=140.209.14.79/32'
    
  }

  stage('Deploy') {

  }

  stage('Test') {

  }

  stage('Delete') {

  }
}
