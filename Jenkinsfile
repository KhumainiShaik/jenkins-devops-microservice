//DECLARATIVE PIPELINE
pipeline{
	agent { 
		docker { 
			image 'maven:3.9.6-amazoncorretto-8-debian-bookworm'
		}
	}
	stages{
		stage('Build'){
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test'){
			steps {
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps {
				echo "Integration Test"
			}
		}
	}
	post{
		always{
			echo 'I am awesome. I run always'
		}
		success{
			echo 'I run when you are successfull'
		}
		failure{
			echo 'I run when you fail'
		}
	}
}