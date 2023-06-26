# gitlab-cicd

Developers performs code commit to one of the feature branch -> Pull Request created for the code Merge -> 
Once it is approved **Code is merged to the Deployment Branch**. Which triggers the **BUILD** creation using tools 
like MAVEN, GRADLE, NPM.
Once the BUILD is created it triggers the **TEST CASES** using tools like Selenium, JUNIT, and the test cases get 
uploaded to the required tool. 
Then it triggers a **SECURITY VULNERABILITY CHECK** along with **STATIC CODE ANALYSIS** usign tools like BLACK DUCK, 
SONARQUBE.
Then BUILDs get uploaded to the Build repository such as sona type NEXUS, JFROG Artifact.
This is the **CONTINUOS INTEGRATION** integrate this together we can use Jenkins, AWS Code Pipeline, GITLAB CI.

As part of the deployment it triggers the deployment to the **DEV** server. Once Sanity is passed deployemtn gets triggered 
to the **UAT** server --> Sanity passed  gets triggered **PROD** server.  This process called **CONTINUOS DELIVER/DEPLOYMENT**
it can  be done using tools like Ansible, HELM, AWS Code Pipeline.

CONTINUOS DEPLOYMENT vs CONTINUOUS DELIVERY
**Continuous Deployment** - need some manual trigger, before the product deployment.
**Continuous Delivery**- automated part of the deployment life cycle.
it is followed by **Continuous Feedback** and **Monitoring** at all stages --> One **RELEASE CYCLE**


