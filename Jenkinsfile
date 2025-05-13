pipeline {
    agent any
    triggers {
        pollSCM('H/2 * * * *') // Polls GitHub every 2 minutes for new commits
    }
    stages {
        stage("Build") {
            steps {
                sh "echo 'Using Gradle to compile and package the Java-based e-commerce application'"
            }
        }
        stage("Unit and Integration Tests") {
            steps {
                sh "echo 'Using JUnit for unit testing and Postman for integration testing of backend APIs'"
            }
        }
        stage("Code Analysis") {
            steps {
                sh "echo 'Using SonarQube to analyse code quality, coding standards, and detect code smells'"
            }
        }
        stage("Security Scan") {
            steps {
                sh "echo 'Using OWASP Dependency-Check to identify known vulnerable dependencies'"
            }
        }
        stage("Deploy to Staging") {
            steps {
                sh "echo 'Using SCP to deploy the application to a staging AWS EC2 instance'"
            }
        }
        stage("Integration Tests on Staging") {
            steps {
                sh "echo 'Using Selenium to run end-to-end integration tests on the staging server'"
            }
        }
        stage("Deploy to Production") {
            steps {
                sh "echo 'Using Ansible to deploy the application to the production AWS EC2 instance'"
            }
        }
    }
}
