pipeline {
    agent any
    environment {
        name = 'suraj'
    }
    parameters {
        string(name: 'person', defaultValue: 'Suraj Soni', description: "who are you?")
    }
    stages {
        stage('Run a commnad') {
            steps {
                sh '''
                ls
                pwd
                cal 2024
                '''
                
            }
        }
        stage('Environmen Variable') {
            steps {
                sh 'echo ${BUILD_ID}'
                sh 'echo ${name}'
            }
        }
        stage('Continue ?') {
            input {
                message "Should we continue?"
                ok "Yes we should"
            }
            steps {
                echo 'deploy on test'
            }
        }
        stage('Deploy to prod') {
            steps {
                echo12 'deploy to prod'
            }
        }
        
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'Failure'
        }
        success {
            echo 'Success'
        }
    }
}
