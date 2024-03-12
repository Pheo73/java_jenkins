pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Execute the build script
                sh './build.sh'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run unit tests
                sh './run_tests.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to production...'
                // Deploy the code to production
                sh './deploy.sh'
            }
            when {
                expression {
                    return env.BRANCH_NAME == 'master'
                }
            }
        }
    }
}
