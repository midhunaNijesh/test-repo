pipeline {
    agent any

    stages {
        stage('validate') {
            steps {
                echo 'validating the code'
                sh '/usr/share/maven/bin/mvn validate'
            }
        }
        stage('Test code') {
            steps {
                echo 'Testing..'
                 sh '/usr/share/maven/bin/mvn test'
            }
        }
        stage('build') {
            steps {
                echo 'Deploying....'
                 sh '/usr/share/maven/bin/mvn package'
            }
        }
    }

}
