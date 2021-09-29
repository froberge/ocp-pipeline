# Install OpenShift Serverless operator

OpenShift Serverless is provided as an add-on on top of OpenShift that can be installed via an operator that is available in the OpenShift OperatorHub.

## Steps:

First, connect to OpenShift console with a user that has Cluster administration right and make sure you are on the Administrator perspective as shown below:
![Administration Perspective](images/admin-perspective.png)

Then, go `Operators -> OperatorHub`. You should now see a list of available operators for OpenShift provided by Red Hat, the community and our partners.
![Operator Hub](images/operator-hub.png)

To facilitate the process, in the `Filter by keyword...`, type OpenShift Serverless to find the required operator:

![Pipeline Operator](images/serverless-operator.png)

Click on the Openshift Serverless operator to start the installation.  Leave the default setting and click install to start the installation process.

![Installation](images/install-serverless.png)

Once the installation is done, you should now see the OpenShift Serverless Operator in the Installed Operators tab, as shown below:

![Installed Operator Tab](images/install-operator-serverless.png)


Now that the installation is done. Let's go into the operator in the knative-serving project to create a Knative Serving as shown below:
![Operator View](images/serverless-operator-view.png)

Create a Knative by selecting the button, leave everything as default.

![Create Knative-serving](images/create-knative-serving.png)

Click create. You should now see the serving as below.
![Create Knative-serving](images/knative-serving.png)

:tada: CONGRATULATIONS 
The operator is now installed on the cluster with a Serving created. Applications can now be deployed as a Knative Service.
![Knative-service](images/resource-deployment-knative.png)


The Serverless option should now be available in the left menu, as shown here:

![Left menu](images/left-menu-serverless.png)