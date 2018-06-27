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
            post {
                always {
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        

    }
}
