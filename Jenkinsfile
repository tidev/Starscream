#! groovy
library 'pipeline-library'

stage('Build') {
	node('osx && xcode-12') {
		checkout scm
		sh './xcframework.sh'
		dir('build/starscream-universal') {
			archiveArtifacts 'Starscream.xcframework/'
		}
	}
}
