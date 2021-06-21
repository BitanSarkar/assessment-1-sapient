pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('Install') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Run') {
            steps {
                script{
                    if ('%gender%' == 'female'){
                        bat 'java -cp target/assessment1-1.0.jar com.sapient.App 2'
                    }
                    else{
                        bat 'java -cp target/assessment1-1.0.jar com.sapient.App 1'
                    }
                }
            }
        }
    }
}
