pipeline {
    agent any
    stages {
        stage('Build svc1') {
            when {
                changeset "**mono/svc1/*.*"
            }
            steps {
            }
        }
        stage('build svc2') {
            when {
                changeset "**mono/svc2/*.*"
            }
            steps {
                echo 'svc2cuy'
            }
        }
    }
}
