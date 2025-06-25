pipeline {
	agent any

	stages {
		stage('Checkout') {
			steps {https://github.com/ajsrDai/model-train.git}
		}
		stage('Install Dependencies') {
			steps{sh 'pipinstall -r requirements.txt'}
		}
		stage('Train Model') {
			steps {sh 'python3 train.py'}
		}
		stage('Test Model') {
			steps {sh 'python3 test.py'}
		}
		stage('Archive Model') {
			steps {archiveArtifacts artifacts: 'model.pkl', fingerprint: true}
		}
	}
}
