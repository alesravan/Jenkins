pipeline{
    agent any
    environment{
        ENV_URL="pipeline.google.com"
        SSHCRED = credentials('SSH_CRED')
    }
    parameters{
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages{
        stage('Stage1'){
            steps{
                    sh '''
                        env 
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