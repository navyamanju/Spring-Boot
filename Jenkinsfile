pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
            
                bat "rmdir /s /q Spring-Boot"
                bat "git clone https://github.com/navyamanju/Spring-Boot.git"
            }
        }
        stage('install') {
            steps {
                dir('Spring-Boot/SpringBootSecurityExample') {
                    bat "mvnw clean install "
                }
            }
        }
        stage('test') {
            steps {
                dir('Spring-Boot/SpringBootSecurityExample') {
                    bat "mvnw test "
                }
            }
        }
        stage('package') {
            steps {
                dir('Spring-Boot/SpringBootSecurityExample') {
                    bat "mvnw package "
                }
            }
        }
    }
}
