pipeline{
    agent any
    stages{
        stage('1-git repo'){
            steps{
                sh 'ls -a'
            }
        }
        stage('2- main'){
           steps{
                sh 'echo "demo job successful"'
            }
        }
        stage('3- parallel jobs'){
            parallel{
                stage('1-subjob'){
                    steps{
                        sh 'lscpu'
                    }
                }
                stage('2-subjob2'){
                    steps{
                        sh 'top -n 2'
                    }
                }
            }
            stage('4-pipelinecheck'){
                steps{
                    sh 'echo " done"'
                }
            }
        }
    }
}