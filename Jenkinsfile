pipeline{
    agent any
    stages{
        stage(1-'git repo'){
            steps{
                sh 'ls -a'
            }
        }
        stage('2-parallel jos'){
            parallel{
                stage('sub job'){
                    steps{
                        sh 'll'
                    }
                }
                stage('sub job2'){
                    steps{
                        sh '$(pwd)'
                    }
                }
            }
            stage('3- main'){
                steps{
                    sh 'echo "demo job successful"'
                }
            }
            stage('4-main'){
                pararell{
                    stage('sub parallejob'){
                        steps{
                            sh 'echo "thank you prof. Elvis"'
                        }
                    }
                    stage('sub paralleljob2'){
                        steps{
                            sh 'top -n 2'
                        }
                    }
                }
                stage('finale stage'){
                    steps{
                        sh 'logname'
                    }
                }
            }
        }
    }
}