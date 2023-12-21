pipeline {
    agent any
    tools {
        maven 'jenkins-maven'
        jdk 'jenkins-java'
    }
    stages {
        stage ('Build') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}
