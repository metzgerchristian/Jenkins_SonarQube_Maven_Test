pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
        jdk '11.0.5'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn clean install sonar:sonar' 
            }
        }
    }
}
