pipeline {
    agent any
    stages {
       
        stage('Build') {
            steps {
                bat 'mvnw package'
            }
            
        }
        post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
        }
    }
}
