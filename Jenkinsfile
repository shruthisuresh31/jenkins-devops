/*
node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Deploy') {
		echo "Deploy"
	}
}
*/

pipeline {
	agent {docker {image 'maven:3.6.3'}}
		  stages{
			  stage("Build"){
				            steps{
                                echo"build stage"
				                }
			                }
			  stage("Test"){
				           steps{
                                echo"test stage"
				              }
			             }
			  stage("Deploy"){
				           steps{
                               echo"deploy stage"
				              }
			                }
		         }

	      post{
		      always{
			          echo"always"
		           }
		      success{
			          echo"success"
		            }
		      failure{
			          echo"failure"
		           }
	         }
      
}