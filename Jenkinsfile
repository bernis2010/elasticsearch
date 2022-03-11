pipeline {
    agent any

    stages {
        
        stage('clean') {
            agent { 
            docker 'image 'openjdk:11''
            }
            
            steps {
               sh '''
                sh "./gradlew build"
                '''
            }
        }

       stage('assemble') {
            agent { 
            docker 'image 'openjdk:11''
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
