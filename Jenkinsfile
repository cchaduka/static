pipeline {
  agent any
  stages {    
    stage ('Upload to AWS') {
      steps {
        withAWS(region:'us-east-2',credentials:'aws-static') {
          sh 'echo "Uploading index.html file to S3 Bucket"'
          s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacityproj04s3bucket01')
        }
      }
    }   
  }
}
