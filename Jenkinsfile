pipeline {
    agent any
    stages {
        stage('clone git repo') {
            steps {
                bat "git clone https://github.com/brajesh9718/cicdpilelinerepo.git"
            }
        }
        stage('clean & install') {
            steps {
                bat "mvn clean install -f cicdpipelineapp/pom.xml"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f cicdwebapp/"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f cicdwebapp/"
            }
        }
    }
}
