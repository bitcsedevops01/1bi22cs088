pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	     }
	stages{
		stage('Checkout'){
		steps{
			git branch:'master',url:'https://github.com/bitcsedevops01/1bi22cs088.git'
		}
	}
		stage('Build'){
		steps{
			sh 'gradle build'
		}
	}
		stage('Test'){
		steps{
			sh 'gradle test'
		}
	}
		stage('Run Application'){
		steps{
			sh 'gradle run'
		     }
	}
}
		post{
			success{
				echo 'Build success'
			       }
			failure{
				echo 'Build failed'
			       }
		    }
	}	
