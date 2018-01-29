
node {
	stage 'Prepare'{
	loadProperties()
	echo "One ${maven} and Second ${java}"
	}
	stage 'Build'{
	  echo "***********Building Code************"  
          echo "*******getting value ${maven}*********"
          bat 'cd C:/learning/software-dump/gradle-4.1-bin/practice'
          bat 'gradle hello1'   
	}

}


def loadProperties() {
   properties = null
       // checkout scm
        properties = new Properties()
        File propertiesFile = new File("${workspace}/gradle.properties")
        properties.load(propertiesFile.newDataInputStream())
        echo "Immediate one ${maven}"
  
}
	 
