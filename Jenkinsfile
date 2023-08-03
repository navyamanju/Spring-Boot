pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
             
            }
        }
        stage('install') {
            steps {
                dir('Spring-Boot/SpringBootSecurityExample') {
                    bat "mvn clean install"
                }
            }
        }
        stage('test') {
            steps {
                dir('Spring-Boot/SpringBootSecurityExample') {
                    bat "mvn test"
                }
            }
        }
        stage('package') {
            steps {
                dir('Spring-Boot/SpringBootSecurityExample') {
                    bat "mvn package"
                }
            }
        }
    }
}
