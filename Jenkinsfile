pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('build') {
            steps {
                git url: 'https://github.com/Kirantubakad/mavenproject.git'
                stash 'source'
            }
        }
        stage('deploy') {
            steps {
                unstash 'source'
                sh  'mvn clean install'
            }
        }
    }
}
