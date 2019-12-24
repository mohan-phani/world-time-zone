pipeline{
	agent any
	stages{
		stage('Build Application'){
			steps{
				bat 'mvn clean install'
			}
		}
		stage('Deploy Application To Mulesoft'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		stage('Perform Regression Testing'){
			steps{
				bat 'newman run E:\\newman\\worldtimezone.postman_collection.json --disable-unicode'
			}
			
		}
	}
}