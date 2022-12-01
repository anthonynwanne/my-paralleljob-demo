pipeline{
    agent any
    stages{
        stage('1-gitrepo'){
            steps{
                sh 'ls -a'
            }
        }
        stage('2-main'){
           steps{
                sh 'echo "demo job successful"'
            }
        }
        stage('3-parallel-jobs'){
            parallel{
                stage('1-subjob'){
                    steps{
                        sh 'lscpu'
                    }
                }
                stage('2-subjob2'){
                    steps{
                        sh 'echo "hello World"'
                    }
                }
            }
        }
        stage('4-jobdone'){
            steps{
                sh 'echo "parallel job done"'
            }
        }
        stage('5-marvinping'){
            parallel{
                stage('1-code2marvin'){
                    steps{
                        sh 'df -h'
                    }
                }
                stage('2-artfactgen'){
                    steps{
                        sh 'echo "my paralell job push to pipeline"'
                    }
                }
                stage('3-push2nexus'){
                    steps{
                        sh 'whoami'
                    }
                }
            }
        }
        stage('5-ansibleintegration'){
            steps{
                sh 'cat /etc/passwd'
            }
        }
        stage('6-buildingdocker'){
            pararell{
                stage('1-dockerimage'){
                    steps{
                        sh 'logname'
                    }
                }
                stage('2-dockercontainer'){
                    steps{
                        sh 'free -m'
                    }
                }
                stage('3-delpoy2dev'){
                    steps{
                        sh 'free -m'
                    }
                }
                stage('4-kubernativeclustertest'){
                    steps{
                        sh 'echo "test successful"'
                    }
                }
            }
        }
        stage('7-deploy2prod'){
            steps{
                sh 'echo "well done Engr. Anthony"'
            }
        }
    }
}