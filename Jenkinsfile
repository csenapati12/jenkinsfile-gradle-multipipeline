pipeline {
    agent { label 'master' }
    stages {
	    
        stage('Clone') {
          steps {
	  echo "******************Cloning code **********"
            checkout scm
          }
       }
       stage('Build') {
          steps {
	     echo '***********Building Code************'  
             bat 'cd C:/learning/software-dump/gradle-4.1-bin/practice'
             bat 'gradle hello1'              
            
          }
       }
	 
    }
}
