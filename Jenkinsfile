pipeline {
    agent any
    stages {
        stage('clean & install') {
            steps {
                bat "mvn clean install -f cicdpipelineapp/pom.xml"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f cicdpipelineapp/"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f cicdpipelineapp/"
            }
        }
    }
}
