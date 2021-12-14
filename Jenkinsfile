pipeline {
	    agent any

		//agent {docker {	image 'maven:3.6.3'	}}
		//agent {docker {	image 'node:13.8'	}}
	enviornment {
		DockerHome tool "mymaven"
		MavenHome  tool "mydocker"
		PATH="$DockerHome/bin:$MavenHome/bin:$PATH"
	}

		stages{
			stage('Build'){
			
				steps{
					echo "Build"
				sh 'mvn --version'
				sh 'node --version'
				echo "$PATH"
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
