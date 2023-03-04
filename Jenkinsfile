pipeline {
    agent { label 'JDK-17' }
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/farheen521/openmrs-core.git',
                    branch: 'declarative'
            }
        }
        stage('package') {
            steps {
                sh 'mvn clean package'
            }
        }