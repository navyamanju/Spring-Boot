pipeline {
    agent any
    environment {
        // Replace '/path/to/java' with the actual path to your Java JDK installation directory
        JAVA_HOME = 'C:/Program Files/Java/jdk17'
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }
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
