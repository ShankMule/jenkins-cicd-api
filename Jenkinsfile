pipeline {  
	agent any 
	stages{ 
		stage('Build Application') { 
		steps { 
			bat 'mvn clean -DskipTests package' 
		} 
		}

		stage('Run Unit Tests') { 
		steps { 
			echo 'Cannot run the Munit test cases because the maven containers are not available in the Jenkins' 
		} 
		}
		
		stage('Deploy CloudHubs') { 
		steps { 
			echo 'Deploying mule project due to the latest code commit…' 
			echo 'Deploying to the configured environment….' 
			bat 'mvn clean deploy -Pdev -DmuleDeploy'
		}  
		} 
		} 
}