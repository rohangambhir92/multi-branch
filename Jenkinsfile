pipeline
{
    agent any
	tools
	{
		maven 'Maven'
	}
	options
    {
        timeout(time: 1, unit: 'HOURS')
		
        // Discard old builds after 5 days or 5 builds count.
        buildDiscarder(logRotator(daysToKeepStr: '5', numToKeepStr: '5'))
	  
	    //To avoid concurrent builds to avoid multiple checkouts
	    disableConcurrentBuilds()
    }
    stages
    {
	    stage ('checkout')
		{
			steps
			{
				//checkout scm
				echo "Checking out on Master Bracnh"
			}
		}
		stage ('Build')
		{
			steps
			{
				//sh "mvn install"
				echo "testing out on Master Bracnh"
			}
		}
		stage ('Unit Testing')
		{
			steps
			{
				//sh "mvn test"
				echo "Tesying out on Master Bracnh"
			}
		}
		
	}
	post 
	{
        always 
		{
			echo "*********** Executing post tasks like Email notifications *****************"
        }
    }
}
