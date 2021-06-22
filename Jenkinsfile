pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('Install') {
            steps {
                cmd 'mvn clean install'
            }
        }
        stage('Run') {
            steps {
                script{
                    if ('%gender%' == 'female'){
                        cmd 'java -cp target/assessment1-1.0.jar com.sapient.App 2'
                    }
                    else{
                        cmd 'java -cp target/assessment1-1.0.jar com.sapient.App 1'
                    }
                }
            }
        }
    }
}
