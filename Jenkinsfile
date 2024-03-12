pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Exécutez les commandes de build ici.
                // Utilisez des commandes compatibles avec Windows
                sh 'C:\\Users\\top20\\Downloads\\apache-maven-3.9.6\\bin\\mvn.cmd clean package'
            }
        }
        stage('Test') {
            steps {
                // Exécutez les tests
                // Utilisez des commandes compatibles avec Windows
                sh 'C:\Users\top20\IdeaProjects\tp_1_test\src test'
            }
        } 
    }
    post {
        success {
            // Actions à effectuer en cas de succès du pipeline
            echo 'Le pipeline a réussi!'
        }
        failure {
            // Actions à effectuer en cas d'échec du pipeline
            echo 'Le pipeline a échoué. Vérifiez les logs pour plus d\'informations.'
        }
    }
}
