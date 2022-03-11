pipeline {
    agent any

    stages {
        
        stage('clean') {
            ls 
            agent { 
            docker {
                    image 'openjdk:11'
                }

            }
            
            steps {
               sh '''
                ./gradlew clean
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
                ./gradlew :distribution:archives:linux-tar:assemble
                ls -l
                '''
            }
        }


    }
}
