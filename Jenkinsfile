pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1',credentials:'aws-static') {
                     // do something
                    s3Upload(file:'index.html', bucket:'static-bucket-jenkins')
                }
                sh 'echo "Upload index.html to the bucket"'
            }
        }
    }
}
