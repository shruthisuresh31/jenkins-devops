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

	parameters{
		choice(name: "Environment", choices: ["dev","test"], description: "Environment")

	}
		  stages{
			  stage("Build"){
				             
				            steps{
                                echo" build stage"
								sh "params.Environment"
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