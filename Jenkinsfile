node()
{
	
	parameters {
        booleanParam(defaultValue: false, description: '', name: 'userFlag')
	string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
    try	{
	        
	        if (env.BRANCH_NAME == 'develop') 
			{
			 print "Building the develop branch "
			 developBranch()
			}
		
	           else if (env.BRANCH_NAME == 'master') 
			{
			 print "Building the master branch "
			//calling the function masterBranch if master branch is getting built
			 masterBranch()
			}
	           else  
			{
			 print "Building the feature branch"
			//calling the function featureBranch if feature branch is getting built
			 featureBranch()
			}
		
		} 
	catch(e) 
		{
		currentBuild.result = "FAILED"	
		//notifyBuild(currentBuild.result)
		throw(e)
		} 
    finally 
		{
		sh "echo final block"
		}	
 }

def developBranch() 
{
 echo "inside DEVELOP"
}

def masterBranch() 
{
 echo "inside MASTER"
}

def featureBranch() 
{
 echo "inside FEATURE"
	stage 'Prepare'
	loadProperties()
	stage 'Checkout'
	checkout_code()
	stage 'Build'
	//withMaven(maven: 'apache Maven 3.3.9'){
	sh 'mvn clean compile'
	//}
}
def loadProperties() {
	echo "Inside Prepare"

        properties = null
        checkout scm
	echo "Immediate one ${userFlag}"
	echo "${params.Greeting} World!"
	 echo  "Branch Name is ${env.BRANCH_NAME}"
       // properties = new Properties()
       // File propertiesFile = new File("${workspace}/gradle.properties")
       // properties.load(propertiesFile.newDataInputStream())
	
       
  
}
def checkout_code()
	{
		echo "checkout_code"
		//checkout scm
	}
def build_code()
	{
	 echo "***********Building Code************"  
          //echo "*******getting value ${maven}*********"
         // sh 'cd C:/learning/software-dump/gradle-4.1-bin/practice'
          //sh 'gradle hello1'   
}


	 
