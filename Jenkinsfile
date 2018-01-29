properties = null
def loadProperties() {
   
       // checkout scm
        properties = new Properties()
        File propertiesFile = new File("${workspace}/gradle.properties")
        properties.load(propertiesFile.newDataInputStream())
        echo "Immediate one ${maven}"
  
}

pipeline {
    agent { label 'master' }
    stages {
	    stage ('Prepare') {
            agent any

            steps {
                script {
                    loadProperties()
			echo "One ${maven} and Second ${java}"
                }
            }
        }
       // stage('Clone') {
       //   steps {
	//  echo "******************Cloning code **********"
       //     checkout scm
      //    }
     //  }
       stage('Build') {
          steps {
	     echo "***********Building Code************"  
		  echo "*******getting value ${maven}*********"
             bat 'cd C:/learning/software-dump/gradle-4.1-bin/practice'
             bat 'gradle hello1'              
            
          }
       }
	 
    }
}
