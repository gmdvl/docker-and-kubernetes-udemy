CODE_CHANGES = getGitChanges(
  'Jenkinsfile',
  'groovy',
  'Section 6/77-shorthand/frontend/Jenkinsfile'
);
pipeline{
    agent{
        label 'master'
    }
    stages{
        stage('Build'){
            when{
                expression{
                    CODE_CHANGES == true
                }
                allOf{
                    status 'success'
                    status 'failure'
                }
            }
            steps{
                sh 'echo "Hello World"'
            }
        }
        stage('Test'){
            steps{
                sh 'echo "Hello World"'
            }
        }
        stage('Deploy'){
            steps{
                sh 'echo "Hello World"'
            }
        }
    }
    before{
        sh 'echo "Hello World"'
        docker build -f Dockerfile.dev -t jenkins-dokcer-dev .
    }
}