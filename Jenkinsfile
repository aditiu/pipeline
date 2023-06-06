pipeline {
    agent any
  
    stages {
        stage('Compile') {
            steps {
                maven(maven : 'Maven 3.5.2'){
                bat 'mvn compile' 
		}
            }
        }
        stage('Test') {
            steps {
               
               maven(maven : 'Maven 3.5.2'){
                bat 'mvn test' 
		}
                
	    }	    
        }
        stage('Package') {
            steps {
                
               maven(maven : 'Maven 3.5.2'){
                bat 'mvn package' 
		}
                 
	    }	    
        }
	
    }
}
