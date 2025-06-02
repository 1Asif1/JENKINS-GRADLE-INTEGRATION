pipeline {
    agent any
    tools{
        jdk 'JDK17'
        gradle 'Gradle 7'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/1Asif1/JENKINS-GRADLE-INTEGRATION.git'
            }
        }

        stage('Build') {
            steps {
                bat 'gradlew.bat build'
            }
        }

        stage('Test') {
            steps {
                bat 'gradlew.bat test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
