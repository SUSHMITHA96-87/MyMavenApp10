pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master',url:'https://github.com/SUSHMITHA96-87/MyMavenApp10.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'java -jar target/MyMavenApp10-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo 'build and deployment successfully!'
		}
		failure{
			echo 'build failed!'
		}
	}
}
