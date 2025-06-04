pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{git branch: master 'https://github.com/chandrashekardn/MavenJenkins1.git'}
		}
		stage('Build'){
			steps{sh 'mvn clean package'}
		}
		stage('Test'){
			steps{sh 'mvn test'}
		}
		stage('Run Application'){
			steps{sh 'java -jar target/.jar'}
		}
	}
	post{
		success{
			echo 'Build and Deployment successful'
		}
		failure{
			echo 'Not done'
		}
	}
	
}
