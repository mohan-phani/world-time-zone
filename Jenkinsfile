pipeline
{
	agent any
	stages
	{
		stage('Build Application'){
			steps{
				bat 'mvn clean install -Dmaven.test.skip=true'
			}
		}
		stage('Munit Test Application'){
			steps{
				bat 'mvn test'
			}
		}
		stage('Deploy Application To Mulesoft'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		stage('Perform Regression Testing'){
			steps{
				bat 'C:\\Users\\DELL\\AppData\\Roaming\\npm\\newman run E:\\newman\\worldtimezone.postman_collection.json --disable-unicode'
			}
			
		}
	}
}