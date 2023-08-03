pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               
                bat "git clone https://github.com/navyamanju/Spring-Boot.git"
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
