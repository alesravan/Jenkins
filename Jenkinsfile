pipeline{
    agent any
    environment{
        ENV_URL="pipeline.google.com"
        SSHCRED = credentials('SSH_CRED')
    }
    stages{
        stage('Stage1'){
            steps{
                    sh '''
                        echo env
                        echo I am at Stage1
                        echo ${ENV_URL}
                    '''
            }
        }

         stage('Stage2'){
             environment{
                        ENV_URL="stage2.google.com"
                    }
            steps{
                sh '''
                    echo I am at Stage2
                    echo ${ENV_URL}
                '''
            }
        }

         stage('Stage3'){
            steps{
                echo "I am at Stage3"
            }
        }
    }
    
}