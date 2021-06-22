pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('Install') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Run') {
            steps {
                script{
                    if ('%gender%' == 'female'){
                        sh 'java -cp target/assessment1-1.0.jar com.sapient.App 2'
                    }
                    else{
                        sh 'java -cp target/assessment1-1.0.jar com.sapient.App 1'
                    }
                }
            }
        }
    }
}
