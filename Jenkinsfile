pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    bat 'C:\\Users\\top20\\Downloads\\apache-maven-3.9.6\\bin\\mvn.cmd clean package'
                }
            }
        }
        stage('Test') {
             steps {
            
            script {
                bat 'C:\\Users\\top20\\Downloads\\apache-maven-3.9.6\\bin\\mvn.cmd test'
            }
        }
    }
    }
    post {
        success {
            echo 'La pipeline a réussi!'
        }
        failure {
            echo 'La pipeline a échoué. Vérifiez les logs pour plus d\'informations.'
        }
    }
}
