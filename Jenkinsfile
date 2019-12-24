pipeline
{
	agent any
	stages
	{
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
				bat 'C: 
				cd cd C:\Users\DELL\AppData\Roaming\npm
				newman run E:\\newman\\worldtimezone.postman_collection.json --disable-unicode'
			}
			
		}
	}
}