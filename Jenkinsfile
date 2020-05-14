pipeline {
    agent any
    stages {
        stage('Lint HTML'){
            steps {
                sh 'echo "Linting the index.html"'
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                sh 'echo "Upload index.html to the bucket"'
                withAWS(region:'us-east-1',credentials:'aws-static') {
                     // do something
                    s3Upload(file:'index.html', bucket:'static-bucket-jenkins')
                }
            }
        }
    }
}
