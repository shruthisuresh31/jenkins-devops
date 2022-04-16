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
	agent any
		  stages{
			  stage("Build"){
				            steps{
                                echo"build stage"
				                }
			                }
			  stage("Test"){
				             when{
								 expression{
									 BRANCH_NAME == "dev"
								 }
							 }
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