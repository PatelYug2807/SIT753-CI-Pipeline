pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application code.'
                echo 'Tool: Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests and integration tests to verify code and component behaviour.'
                echo 'Tool: JUnit (unit tests), Postman/Newman (integration tests)'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse code quality and maintainability against industry standards.'
                echo 'Tool: SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Task: Scan the codebase and dependencies for known vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a staging environment.'
                echo 'Tool: AWS EC2 (staging instance)'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests against the staging deployment.'
                echo 'Tool: Selenium'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the application to the production environment.'
                echo 'Tool: AWS EC2 (production instance)'
            }
        }
    }
}