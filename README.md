# GitLab-cicd

Developers perform code commit to one of the feature branches -> Pull Request created for the code Merge -> 
Once it is approved **Code is merged to the Deployment Branch**. Which triggers the **BUILD** creation using tools 
like MAVEN, GRADLE, and NPM.
Once the BUILD is created it triggers the **TEST CASES** using tools like Selenium, JUnit, and the test cases get 
uploaded to the required tool. 
Then it triggers a **SECURITY VULNERABILITY CHECK** along with **STATIC CODE ANALYSIS** using tools like BLACK DUCK, 
SONARQUBE.
Then BUILDs get uploaded to the Build repository such as sona type NEXUS, and JFROG Artifact.
This is the **CONTINUOUS INTEGRATION** integrate this together we can use Jenkins, AWS Code Pipeline, and GitLab CI.

As part of the deployment, it triggers the deployment to the **DEV** server. Once Sanity is passed deployment gets triggered 
to the **UAT** server --> Sanity passed  gets triggered to **PROD** server.  This process called **CONTINUOUS DELIVER/DEPLOYMENT**
it can  be done using tools like Ansible, HELM, and AWS Code Pipeline.

CONTINUOUS DEPLOYMENT vs CONTINUOUS DELIVERY
**Continuous Deployment** - need some manual trigger, before the product deployment.
**Continuous Delivery**- automated part of the deployment life cycle.
it is followed by **Continuous Feedback** and **Monitoring** at all stages --> One **RELEASE CYCLE**

![lifecycle](1.png)


**GitLab RUNNER** is an application that runs jobs in a pipeline, and can be installed on the cloud or an on-prem,
can be installed on many different operating systems, and runs on DOCKER and K8S. 
DEVOPS person registers an agent with a token, established a trust relationship between GitLab Instance and communication channel, 
TYPES of RUNNER: 
Private Runner - like the self-hosted agent and can be installed on your own data center or cloud services. 
Shared Runner - uses the runner from the available pool of runners, GitLab based on tags. 
GROUP Runner - can be installed on Kubernetes cluster which supports high availability and fault tolerant. 



