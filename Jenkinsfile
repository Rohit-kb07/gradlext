pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages{
	    stage('checkout'){
		steps{
		git branch : 'master' ,url:'https://github.com/Rohit-kb07/gradlext.git'
		}
	     }
	     
	     stage('build'){
	        steps{
	           sh 'gradle build'
	           }
	       }
	       
	     stage('Test'){
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
	         echo 'build succesful'
	         }
	     failure{
	         echo 'build failed'
	         }
	 }
}	 
	     
	     
	     
	     
	     
	     
	     
	     
