pipeline{
    agent any
    stages{
        stage('1-git clone'){
            parallel{
                steps{
                    sh 'echo "welcome"'
                }
            }
            stage('sub stage1'){
                steps{
                    sh 'touch pipeline'
                }
            }
        }
        stage('2-git pull'){
            steps{
                sh 'df -h'
            }
        }
        stage('3-main stage3'){
            parallel{
                steps{
                    sh 'ls -a'
                }
            }
            stage('sub stage3'){
                steps{
                    sh 'll'
                }
            }
            stage('sub stage 3b'){
                steps{
                    sh 'echo "sub stage 3"'
                }
            }
        }
        stage('4-pipeline check'){
            steps{
                sh '$(pwd)'
            }
        }
    }
}