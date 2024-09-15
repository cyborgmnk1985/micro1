pipeline {
    agent any
    stages{
        stage('Hello'){
            steps{
                echo "Hello from jenkis file micro 1"
            }
        }
        stage('for the fix branch'){
            when{
                branch "fix-*"
            }
            steps{
                sh '''
                    cat README.md
                '''
            }
        }
        stage('for the PR'){
            when{
                branch "PR-*"
            }
            steps{
                echo 'this only runs for the PRs'
            }
        }
    }
}