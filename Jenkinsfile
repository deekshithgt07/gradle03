pipeline {
	agent any 
	
	tools{
	gradle 'Gradle'
	jdk 'JDK'
	}
	stages{
	stage('Checkout'){
		steps{
		git branch: 'master', url: 'https://github.com/deekshithgt07/gradle03.git'
		}
	}
	stage('Build'){
	steps{
	sh 'gradle build'
	}
	}
	stage('test'){
	steps{
	sh 'gradle test'
	}
	}
	
	stage('Run application'){
	steps{
	sh 'gradle run'
	}
	}
	
	}
	post{
		success{
			echo 'Build and deployment successful!'
		}
		failure{
			echo 'Build failed!'
		}
	}
}
