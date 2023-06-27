pipeline{
    agent any
    environment{
        ENV_URL="pipeline.google.com"
    }
    stages{
        stage('Stage1'){
            steps{
                    sh ```
                        echo I am at Stage1
                        echo ${ENV_URL}
                    ```
            }
        }

         stage('Stage2'){
            steps{
                echo "I am at Stage2"
            }
        }

         stage('Stage3'){
            steps{
                echo "I am at Stage3"
            }
        }
    }
    
}