pipeline {
    agent any
        tools {
        jdk "java_8"
        maven "maven_354"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit '/home/vagrant/workspace/jenkinsfiletest/target/surefire-reports.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                //sh './jenkins/scripts/deliver.sh'
                sh 'echo test'
            }
        }
    }
}
