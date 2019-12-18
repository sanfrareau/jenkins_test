pipeline {
	agent any

	stages {

        stage('Clean') {
            steps {
                echo 'Clean..'
                gradlew('clean', 'classes')
            }
        }

	}
}