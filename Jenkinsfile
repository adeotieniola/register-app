pipeline {
    agent {label 'Jenkins-Agent'}
    tools {
        jdk 'Java21'
        maven 'Maven3'
    }
    stages{
        stage{"Cleanup Workspace"}{
                steps {
                cleanws{}
                }
        }

        stage{"Checkout from SCM"}{
                steps {
                    git branch: 'main', credentialId: 'github', url: 'https://github.com/adeotieniola/register-app'
                }
        }
        
        stage{"Build Application"}{
            steps {
                sh 'mvn clea pacakage'
            }
        }

        stage{"Test Aplication"}{
             steps {
                   sh 'mvn test'
             }  
        }
   }

}
