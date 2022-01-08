pipeline {
    agent any

    stages {
        stage('continuous download') {
            steps {
                git 'https://github.com/Rajesh1967/boxfuse-sample-java-war-hello.git'
            }
        }
        stage('continuous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continuous deploy') {
            steps {
                sh 'sshpass -p "rajesh" scp target/hello-1.0.war rajesh@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
