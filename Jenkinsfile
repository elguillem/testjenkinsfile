pipeline {
    agent any
        tools {
        jdk "java_8"
        maven "maven_354"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
           stage('stage2') {
                steps {
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        

    }
}
