pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('Install') {
            steps {
                bat 'echo %gender%'
                bat 'mvn clean install'
            }
        }
        stage('Run') {
            steps {
                bat 'java -cp target/assessment1-1.0.jar com.sapient.App'
            }
        }
    }
}
