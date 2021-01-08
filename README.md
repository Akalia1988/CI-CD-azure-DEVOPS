# CI-CD-azure-DEVOPS
Pipeline for .netcore apps, Azure functions and we will introduce SONARQUBE, Azure key vault and OWASP for penetration testing

Azure DevOps project automatically configured a full CI/CD pipeline in your Azure DevOps organization. You can explore and customize the pipeline as needed. Follow the steps below to familiarize yourself with the Azure DevOps build and release pipelines.

Select Build Pipelines from the top of the Azure DevOps project dashboard. This link opens a browser tab and the Azure DevOps build pipeline for your new project.

in this pane, you can examine the various tasks for your build pipeline. This build pipeline performs various tasks such as fetching sources from the Git repository, restoring dependencies, compile the application, run tests and publishing outputs used for deployments. we will introduce ASP.NET core app and azure key vault template. 

![image](https://user-images.githubusercontent.com/58148717/104059529-1fd94900-51bb-11eb-8f73-d6250bb482f9.png)

![image](https://user-images.githubusercontent.com/58148717/104059602-3a132700-51bb-11eb-8858-90854651bf50.png)



Select Triggers. Azure DevOps project automatically created a CI trigger, and every commit to the repository initiates a new build. You can optionally choose to include or exclude branches from the CI process.

![image](https://user-images.githubusercontent.com/58148717/104059690-58792280-51bb-11eb-908b-5db1b61f32c9.png)

Select Releases under Pipelines section.

![image](https://user-images.githubusercontent.com/58148717/104059800-7f375900-51bb-11eb-866c-8b859e763361.png)

if you are deploy the solution on-prem VM'S or cloud hosted VM's make sure to create the deployment group and execute the powershell script on LINUX, or Windows server. 

![image](https://user-images.githubusercontent.com/58148717/104060028-e81ed100-51bb-11eb-99f5-0f98f7b64579.png)

Afterwards it will look like snip below.

![image](https://user-images.githubusercontent.com/58148717/104060279-48157780-51bc-11eb-962e-29e2917ed95c.png)

From deployment group you can select respective environment and create the release. 

![image](https://user-images.githubusercontent.com/58148717/104060549-af332c00-51bc-11eb-89e9-7b66fce3a1ce.png)

you could release the same code base to Azure app services as well you would need to select Deploy Azure App service from the templates and fill up the rest of the template.

![image](https://user-images.githubusercontent.com/58148717/104060905-3c768080-51bd-11eb-8b96-4af5520e36e2.png)

Pipeline for Azure functions.

In Function app window select Functions. Click on +Add and select Http trigger from the templates.

![image](https://user-images.githubusercontent.com/58148717/104061029-6fb90f80-51bd-11eb-9343-9f63c46b14bc.png)

from Azure Devops select azure app services template and follow the exact steps as we have described above. 

once we are ready to create release we would need to select Azure functions template instead of the app services one after selecting the appropirate template we will good to create the release for furhter clarification https://docs.microsoft.com/en-us/azure/devops/pipelines/targets/azure-functions?view=azure-devops&tabs=dotnet-core%2Cyaml

![image](https://user-images.githubusercontent.com/58148717/104061208-c4f52100-51bd-11eb-819e-38a61053541c.png)


Intoduction of sonarqube. 

First we will learn what is the sonarqube?
SonarQube is an open-source platform developed by SonarSource for continuous inspection of code quality. Sonar does static code analysis, which provides a detailed report of bugs, code smells, vulnerabilities, code duplications.

it's easy to add non-disruptive code quality checks right into your Azure DevOps workflow. Simply add SonarQube to your build pipeline definition and you're on your way to only promoting quality code. SonarQube analyzes the code changes and decorates Pull Requests with comments and overall status.

![image](https://user-images.githubusercontent.com/58148717/104061794-e276ba80-51be-11eb-8066-cd5cf15163fd.png)




































