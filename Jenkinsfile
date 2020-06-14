pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'export MAVEN_HOME=/opt/maven'
                sh 'export PATH=$PATH:$MAVEN_HOME/bin'
                sh 'mvn --version'
                // sh 'mvn clean package'
            }
            post {
                success 
                {
                   /*  echo 'Now Archiving..'
                archiveArtifact artifacts: '**/target/*.war' */
                }
                 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}