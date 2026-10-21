
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                    set "JAVA_HOME=C:\\Users\\Dell\\AppData\\Local\\Programs\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot"
                    set "PATH=%JAVA_HOME%\\bin;%PATH%"
                    "C:\\Program Files\\apache-maven-3.10.0-bin\\apache-maven-3.10.0\\bin\\mvn.cmd" clean package
                '''
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'target/*.jar'
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
