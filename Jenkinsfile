pipeline {
	agent any
	stages {
		
		 ('OWASP DependencyCheck') {
			steps {
				dependencyCheck additionalArguments: '--format HTML --format XML --disableYarnAudit', odcInstallation:'Default'
			}
		}

	}
	post {
		success {
			dependencyCheckPublisher pattern: '**/dependency-check-report.xml'
		}
	}

}
