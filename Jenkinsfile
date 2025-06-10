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
				bat 'mvn clean deploy -DmuleDeploy -X -DskipTests -DmuleVersion=4.6.2n -DappName=jenkins-ci-cd -Denvironment=Sandbox -DdeploymentTimeout=6000000 -Dusername=sewlesewb -Dpassword=Sewlesew1234 -Denvironment=Sandbox -Dbusiness=ethiopian-airlines-5 -DvCore=Micro -Dworkers=1 -DdeploymentTimeout=6000000'
				}
			}
		}
	}

