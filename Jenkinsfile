pipeline {
    agent any
     tools {
        maven 'Maven 3.5.2'
    }
    stages {
        stage('Compile') {
            steps {
          
                sh 'mvn compile' 
                	
            }
        }
        stage('Test') {
            steps {
               
                sh 'mvn test' 
                
	    }	    
        }
        stage('Package') {
            steps {
                
                sh 'mvn package' 
                 
	    }	    
        }
	stage('Deploy') {
            steps {
                echo 'Deploying....'
	      build job: 'AutomatedDeploymentTest'
            }
        }
    }
}
