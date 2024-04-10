pipeline {
    agent any
	
	
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/subha130604/sample.git'
            }
        }
         stage('Build') {
            steps {
                

                 {
			bat 'mvn compile'
                    bat 'mvn package'
			
                }
            }
        }
	    stage('Test'){
		    steps{
			    {
			    bat 'mvn test'
		    }
		    }
	    }
       
        
        stage('Run') { 
            steps {
	    {
                bat "java -cp target/classes com.mycompany.app.App 2"
            }
	    }
        }
        // Add more stages as needed
    }
}
