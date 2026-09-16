pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application. Tool: Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit and integration tests. Tools: JUnit and Selenium.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse code quality and coding standards. Tool: SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan the application for known vulnerabilities. Tool: OWASP Dependency-Check.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a staging server. Tool: AWS CodeDeploy with EC2.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Test the application in the staging environment. Tool: Postman Newman.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the tested application to production. Tool: AWS CodeDeploy with EC2.'
            }
        }
    }
}
