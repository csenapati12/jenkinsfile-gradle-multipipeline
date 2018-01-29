pipeline {
    agent { label 'master' }
    stages {
	    
        stage('Clone') {
          steps {
            chkout scm
          }
       }
       stage('build') {
          steps {
             bat 'cd C:/altisource/software-dump/gradle-4.1-bin/practice'
             bat 'gradle hello1'
              //Created new branch
			  //Merging with the master
               echo 'Example'          
             echo 'not using shell'
          }
       }
	 
    }
}
