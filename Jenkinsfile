pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('build') {
            steps {
                git url: 'https://github.com/Havoc13Naveen/calculator.git'
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
