pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                withMaven(maven : 'Maven 3.5.2'){
                sh 'mvn compile' 
                }	
            }
        }
        stage('Test') {
            steps {
                withMaven(maven : 'Maven 3.5.2'){
                sh 'mvn test' 
                }
	    }	    
        }
        stage('Package') {
            steps {
                withMaven(maven : 'Maven 3.5.2'){
                sh 'mvn package' 
                 }
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
