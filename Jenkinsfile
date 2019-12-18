#!/usr/bin/groovy

pipeline {
	agent any

    options {
        disableConcurrentBuilds()
        }

	stages {

        stage('Clean') {
            steps {
                echo 'Clean..'
                gradlew(clean)
            }
        }

        stage('Unit Tests') {
            steps {
                echo 'Unit Tests..'
                sh '''
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
                    sh '''
                    ./gradlew build
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }

        stage('Automated Test') {
                    steps {
                        echo 'Testing..'
                    }
                }
    }
}

def gradlew(command) {
    sh '''
        ./gradlew ${command}
    '''
}