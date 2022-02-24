pipeline {
    agent any

    stages {
        
        stage('clean') {
            agent { 
            docker 'gradle:7.4.0-jdk17'
            }
            
            steps {
               sh '''
                gradle clean
                '''
            }
        }

       stage('assemble') {
            agent { 
            docker 'gradle:7.4.0-jdk17'
            }
            
            steps {
               sh '''
                gradle :distribution:archives:linux-tar:assemble
                '''
            }
        }


    }
}
