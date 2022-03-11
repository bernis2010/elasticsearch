pipeline {
    agent any

    stages {
        
        stage('clean') {
            agent { 
            docker {
                    image 'openjdk:11'
                }

            }
            
            steps {
               sh '''
                ./gradle clean
                '''
            }
        }

       stage('assemble') {
            agent { 
           docker {
                    image 'openjdk:11'
                }

            }
            
            steps {
               sh '''
                ./gradle :distribution:archives:linux-tar:assemble
                ls -l
                '''
            }
        }


    }
}
