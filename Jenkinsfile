pipeline {
	agent any
	tools {
        maven 'mvn'
	}
	stages {
        stage("Checkout") {   
            steps {                    
                git url: 'git@github.com:mratpa/LearnDevOps.git'               

            }    
        }
        stage('Build') {
            steps {
               dir('calculator') {
                sh "mvn compile"      
               }
            }
        }
        
        stage("Unit test") {               
            steps {      
                 dir('calculator') {
                sh "mvn test"   
                 }            
           }
        }
	}
}