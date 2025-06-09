pipeline{
	agent any
	stages {
		stage('Build Application') {
			steps {
				bat 'mvn clean install'
				}
			}
		stage('Deploy CloudHubs') {
			environment {
				ANYPOINT_CREDENTIALS = credentials('d81e9a97-b416-4975-8680-b8c28e3a080e')
						}
			steps {
				echo 'Deploying mule project due to the latest code commit…'
				echo 'Deploying to the configured environment….'
				bat 'mvn clean deploy -DmuleDeploy -Dmule.app.name=jenkins-ci-cd-Dusername=sewlesewb -Dpassword=Sewlesew@21 -DtargetName=Cloudhub-US-East-1'
				}
			}
		}
	}
