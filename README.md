


## Getting Started Guide

This example demonstrate a sample CI/CD pipeline for API Management using [WSO2 API Management](https://wso2.com/api-management/) solution combined with Travis CI and Newman.

This is implemented based on the [solution](https://github.com/manjulaRathnayaka/API-Management-CI-CD-Example) done by [manjulaRathnayaka](https://github.com/manjulaRathnayaka) for WSO2 API Cloud. Full credits goes to him!.

![](https://github.com/malinthaprasan/APIMCICDExample/raw/master/Architecture.jpg)

  
# To try out this with your repository

1.  Fork this git repository.
    
2.  Configure Dev environment.

	Update DevEnvironment/Development.postman_environment.json to set your Dev Environment's servlet URL (serverURL), gatewayURL.
  
3.  Configure Staging environment.

	Update StagingEnvironment/Staging.postman_environment.json to set your Staging Environment's servlet URL (serverURL), gatewayURL.
  

4. Commit and push above changes to git repository.
    
5.  Configure Travis	
    1. Go to [https://travis-ci.org/](https://travis-ci.org/) and sign in
    with Github.
    	    
    2. Allow permissions to let travis to access your forked repository.
    	    
    3.  Go to your profile and select the GitHub account and the forked repository to enable building your repository.
    
    4.  If the build is not started yet, commit a minor change to your git repository to start it.

    

That is it. Now you can refer the build log to understand the execution flow. Note that this is a very simple .travis.yml configuration and you may use advanced features of travis to configure different states etc.


Now the API should be deployed in both Dev and Staging environments. Now let’s do some changes to the API and propagate those changes to Dev, Staging environments.

1.  Update the swagger file at DeployAPI/swagger.json. Note that you need to have info section in swagger file.
    
2.  Commit and push all above changes and monitor the travis build.

