pipeline {
    agent any

    stages {
        agent { 
            docker 'gradle:7.4.0-jdk17'
            }
        stage('Hello') {
            
            steps {
               sh '''
                gradle clean
                '''
            }
        }
    }
}
