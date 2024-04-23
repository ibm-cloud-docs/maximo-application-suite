---

copyright:
  years: 2024
lastupdated: "2024-04-24"

keywords:

subcollection: maximo-application-suite

---


{{site.data.keyword.attribute-definition-list}}

# Deploying {{site.data.keyword.prodname_imas_short}} deployable architecture
{: #deploying-da}

You can deploy a deployable architecture from the {{site.data.keyword.cloud_notm}} catalog. You can choose among different deployment options, including with {{site.data.keyword.cloud_notm}} projects. [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

## Deploying with {{site.data.keyword.cloud_notm}} projects
{: #maximo-application-suite-deploy-cloud}

To deploy the {{site.data.keyword.prodname_imas_full}} deployable architecture through the {{site.data.keyword.cloud_notm}} catalog, follow these steps:

1. Make sure that you comply with the prerequisites in the [planning](/docs/maximo-application-suite?topic=maximo-application-suite-planning) topic.

1. Go to the {{site.data.keyword.cloud}} catalog and search for the {{site.data.keyword.prodname_imas_short}} deployable architecture that you're interested in deploying.

1. In the search result, click the tile of {{site.data.keyword.prodname_imas_short}} deployable architecture to open the details.

1. Select the latest product version in the Architecture section.

1. Select the variation as Existing Cluster.

1. Click Review deployment options.

1. Select the Add to project deployment type in Deployment options.

1. Create a new project by entering name your project, description, and specify a configuration name. Select the same Region where existing cluster is running. Click Create.

 An existing project can be used by clicking "Add to existing" and then selecting the project and entering the configuration name.
 {: note}

1. Edit and validate the configuration:
 - Select your authentication method. You can use an existing secret in Secrets Manager or add your API key directly. For more information, see Using an API key or secret to authorize projects.
   Enter values for following other required fields from the **Required** tab.
   - cluster_id : Enter Id of the target IBM Cloud Red Hat OpenShift Cluster. This cluster Id can be found under OpenShift clusters section.
   - region : Enter region of the target IBM Cloud Red Hat OpenShift Cluster.
   - mas_entitlement_key : Enter entitlement key to access Maximo Application Suite Image registry. See planning & preparing topic on how to get entitlement key.
    You can use an existing secret in Secrets Manager or add your entitlement key directly.
   - mas_license : Enter Maximo Application Suite License file content. See planning & preparing topic on how to get license file.
    You can use an existing secret in Secrets Manager or add your license file content directly in base64 encoded format.
   - sls_license_id : Enter the Suite License Server license ID. See planning & preparing topic on how to find SLS license Id.
    You can use an existing secret in Secrets Manager or add your SLS License Id directly.
   - deployment_flavour : Enter core for Maximo Application Suite Core deployment and enter manage for Maximo Application Suite Core + Manage deployment.
   - mas_instance_id : Enter the Maximo Application Suite instance Id for instance creation.
   - uds_contact_email : Enter the email ID for Data Reporter Operator.
   - uds_contact_firstname : Enter your first name to be used in Data Reporter Operator.
   - uds_contact_lastname : Enter your last name to be used in Data Reporter Operator.

   Enter the following information in the **Optional** tab
   - mas_workspace_id : Enter the Maximo Application Suite workspace Id. Default value is wrkid1.
   - mas_workspace_name : Enter the workspace name. Default value is wrkns1.
   - storage_class_rwo : Enter the storage class (read-write once). Default value is ibmc-vpc-block-retain-10iops-tier.
    Make sure this storage class is present under **Storage > StorageClasses** section on your Openshift cluster section.
   - storage_class_rwx : Enter the storage class (read-write many). Default value is ibmc-vpc-file-dp2.
    If you are planning to deploy Maximo Application Suite Core + Manage then enter file storage class for DB2 and make sure this storage class is present under **Storage > StorageClasses** section on your Openshift cluster section.
    {: note}

   - pipeline_storage_class : Enter the storage class for pipeline. Default value is ibmc-vpc-block-retain-10iops-tier.
    Make sure this storage class is present under **Storage > StorageClasses** section on your Openshift cluster section.
   - cluster_config_endpoint_type : Enter which type of endpoint to use for for cluster config access: 'default', 'private', 'vpe', 'link'. 'default' value will use the default endpoint of the cluster.
   - Save the configuration.
   - Click Validate. Validation takes a few minutes.
    IBM Cloud projects runs a Code Risk Analyzer scan that includes a supported set of Security and Compliance Center rules. Controls that are part of the deployable architecture and that are also supported by IBM Cloud projects are checked. Any extra controls that are not included in the list of supported Security and Compliance Center rules are not checked when you validate the configuration.
    If the validation fails because of the Code Risk Analyzer scan, you can troubleshoot the failure.

1. Deploy the configuration:
   After you validate your configuration, you can deploy it to your target account.
   1. Review the input values and make any necessary changes.
   1. Click Deploy.
     Deploying the deployable architecture for Maximo Application Suite can take around an hour. For Maximo Application Suite Core + Manage, it can take around 4 to 5 hours.
     You are notified when the deployment is complete and with successful or failure message. In case of failure, refer the schematics log.
1. Review the outputs from the deployable architecture.
 - pipeline_execution_status : If installation pipeline is successful then "Successful" message is shown here. If there is a failure in any of pipeline task then that failed task information will be shown here.
 - maximo_admin_url : If pipeline_execution_status is successful then admin URL to the deployed offering is displayed here.
   Login credentials to this admin url can be found under Workloads > Secrets section on your Openshift cluster. Search for <instance_id>-credentials-superuser name under Secrets section.
   {: note}

   For example, if you entered inst1 as input value to mas_instance_id input field then search for inst1-credentials-superuser name under Secrets section.
