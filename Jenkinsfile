pipeline {
    agent any

    tools {
        gradle 'gradle' // Ensure this name matches the Gradle installation in Jenkins (Manage Jenkins → Global Tool Configuration)
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Bhagyalakshmi-R2005/HelloWorldGradle.git'
            }
        }

        stage('Build') {
            steps {
                bat 'gradle clean build'
            }
        }

        stage('Test') {
            steps {
                bat 'gradle test'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -jar build/libs/HelloGradle-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
