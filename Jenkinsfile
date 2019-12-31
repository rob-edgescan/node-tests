#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'yarn install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'yarn test'
            }
        }
    }
}
