pipeline {
    agent any
    stages {
        def mvnHome
        stage('check enviornment') {
            steps {
               bat 'echo %PATH%'
                mvnHome='echo %MAVEN_HOME%'
            }
        }
        stage('build') {
            steps {
                echo mvnHome
               bat(/"${mvnHome}\bin\mvn" clean package install/);
            }
        }
    }
}
