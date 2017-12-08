# Cloud Foundry Application Sample 

With this template you can provision and manage a Cloud Foundry application. The template here is a sample which, beside the terraform configuration file, also includes the source code of a sample application. This source code is pushed to the IBM Cloud during deployment (i.e. if you trigger the **Apply**, see below).

In order to use this in a scenario where the source code of the application is updated regularly and re-deployed to the cloud, you should fork the repository - or create your own git repo using the terraform configuration files of this template as sample.

## Variables used in this template 

The following variables are used to customize the template. 

| Variable Name | Description | Default Value |
|---------------|-------------|---------------|
|ibm_cloud_apikey|IBM Cloud user apikey| - |
|ibm_cloud_organization|IBM Cloud organization name| - |
|ibm_cloud_space|IBM Cloud space name| - |
|application_hostname|hostname for the application's route. The resulting url will be `hostname.mybluemix.net`. Note that this must be unique across IBM Cloud, i.e. specifying trivial names such as `test` most probably results in an error during deployment. You then have to change the variable and trigger the **Apply** again.| - |
|application_version|version specification of the application. A change of this parameters is an indication for terraform that the application code has changed and needs to be redeployed.|`100`|
|application_instances|number of cloud foundry application instances to be deployed|`1`|

## Next steps

After setting up your environment with this template, you can run **Plan** to preview how Schematics will deploy resources (in this case, a Cloud Foundry application) to your environment. When you are ready to deploy the app, run **Apply**.

After a successful deployment, you can access the application using the provided hostname: `https:\\<hostname>.mybluemix.net`. The exact hostname is also written to the terraform log for reference.  
