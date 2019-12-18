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

	}
}