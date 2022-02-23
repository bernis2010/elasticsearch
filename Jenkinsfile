pipeline {
    agent any

    stages {
        
        
        stage('Hello') {
            
            steps {
               sh '''
                ls -l 
                '''
            }
        }
        
        
        
        stage('Hello') {
            agent { 
            docker 'gradle:7.4.0-jdk17'
            }
            
            steps {
               sh '''
                gradle clean
                gradle assemble
                '''
            }
        }
    }
}
