pipeline {
    agent any

    stages {
        
        stage('clean') {
            agent { 
            docker 'gradle:7.4.0-jdk17'
            }
            
            steps {
               sh '''
                sh "./gradlew build"
                '''
            }
        }

       stage('assemble') {
            agent { 
            docker 'gradle:7.4.0-jdk17'
            }
            
            steps {
               sh '''
                 ./gradlew assemble
                ls -l
                '''
            }
        }


    }
}
