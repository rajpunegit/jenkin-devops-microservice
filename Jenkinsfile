pipeline {
	 agent any

		//agent {docker {	image 'maven:3.6.3'	}}
		//agent {docker {	image 'node:13.8'	}}
	environment {
		mavenHome = tool 'mymaven'
		dockerHome = tool 'mydocker'
		PATH="$mavenHome/bin;$PATH"
	}

		stages{
			stage('Build'){
			
				steps{
					echo "Build"
					echo "$PATH"
				
			  	//sh 'docker version'
				//sh 'mvn --version'
				echo "Build Number - $env.BUILD_NUMBER"
				echo "Build TAG - $env.BUILD_TAG"
				}
				
			}
			stage('Test'){
			
				steps{
					echo "Test"
				}
			}
			stage('Integration Test'){
			
				steps{
					echo "Integration Test"
				}
			}
		}
		post{
			always{

				echo "Always Run"
			}
			success{

				echo "After Success"
			}
			failure{

				echo "After Failure"
			}
		}


	
		
}
