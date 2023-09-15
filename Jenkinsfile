/*
 See the documentation for more options:
 https://github.com/jenkins-infra/pipeline-library/
*/
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/rcpokorny/hello-world-pipeline.git'
                sh 'cd /var/jenkins_home/workspace/TestJava/demo'
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage("Hello") {
            steps {
                greet name: 'Bob Pokorny', useUpperCase: true
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
