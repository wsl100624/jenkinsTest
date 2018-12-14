node('linux') {
  stage('Create') {
    git credentialsId: 'd33c67f2-739d-4210-82d1-ce3c2c0a4e5d', url: 'https://github.com/wsl100624/jenkinsTest.git'
    
    withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: '227bc396-0603-41fb-900c-98a3519fa21f', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
      //sh 'aws cloudformation create-stack --stack-name final-test --template-body file://./docker-single-server.json --region us-east-1 --parameters ParameterKey=KeyName,ParameterValue=seis665 ParameterKey=YourIp,ParameterValue=140.209.14.79/32'
			sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name final-test'
		}    
  }

  stage('Deploy') {

  }

  stage('Test') {

  }

  stage('Delete') {

  }
}
