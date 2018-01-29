node()
{
    try	{
	    stage'select the build type'
	    echo  "Branch Name is ${env.BRANCH_NAME}"
	        if (env.BRANCH_NAME == 'develop') 
			{
			 print "Building the develop branch "
			//calling the function developBranch if develop branch is getting built
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





	 
