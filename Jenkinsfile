pipeline {
	agent any

	stages {

        stage('Clean') {
            steps {
                echo 'Clean..'
                sh '''#!/bin/bash
                    ./gradlew clean
                '''
            }
        }

        stage('Unit Tests') {
            steps {
                echo 'Unit Tests..'
                sh '''#!/bin/bash
                     ./gradlew test
                '''
            }
            post {
                always {
                    junit '**/build/test-results/test/TEST-*.xml'
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Build..'
                    sh '''#!/bin/bash
                    ./gradlew build
                '''
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