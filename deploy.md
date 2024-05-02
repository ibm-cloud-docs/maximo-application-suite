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
{: shortdesc}

## Deploying with {{site.data.keyword.cloud_notm}} projects
{: #maximo-application-suite-deploy-cloud}

To deploy the {{site.data.keyword.prodname_imas_full}} deployable architecture through the {{site.data.keyword.cloud_notm}} catalog, follow these steps:

1. Make sure that you comply with the prerequisites in the [planning](/docs/maximo-application-suite?topic=maximo-application-suite-planning) topic.
1. Select the **Add to project** deployment type in **Deployment** options.
1. Create a project by entering the name of your project, description, and specify a configuration name. Select the same Region where the existing cluster is running.
1. Click Create.
   An existing project can be used by clicking **Add to existing** and then selecting the project and entering the configuration name.
   {: note}

1. Edit and validate the configuration:
   - Select your authentication method. You can use an existing secret in **Secrets Manager** or add your **API key** directly.
    For more information, see [Using an API key with secrets manager to authorize a project to deploy an architecture](/docs/secure-enterprise?topic=secure-enterprise-authorize-project).
   1. Enter values for other required fields in the **Required** tab.
   1. Enter the values for the fields in the **Optional** tab.
1. Save the configuration.
1. Click **Validate**. Validation takes a few minutes.
     {{site.data.keyword.cloud}} projects run a Code Risk Analyzer scan that includes a supported set of Security and Compliance Center rules. Controls that are part of the deployable architecture and that are also supported by {{site.data.keyword.cloud}} projects are checked. Any extra controls that are not included in the list of supported Security and Compliance Center rules are not checked when you validate the configuration.
         If the validation fails because of the Code Risk Analyzer scan, you can troubleshoot the failure. Make sure that validation completes and `Validation successful` message is displayed.
   - In the **Approval pending** section, enter `I approve` and click **Approve**.
1. Deploy the configuration. After you validate your configuration, you can deploy it to your target account.
   1. Review the input values and make any necessary changes.
   1. Click **Deploy**.
       Deploying the deployable architecture for {{site.data.keyword.prodname_imas_short}} can take around an hour. For {{site.data.keyword.prodname_imas_short}} Core + Manage, it can take around 4 to 5 hours.
       You are notified when the deployment is complete and with successful or failure message. In case of failure, refer to the schematics log.
1. Review the outputs from the deployable architecture.
   - **maximo_admin_url** : The admin URL to the deployed offering is displayed here.
     Login credentials to this admin url can be found under the **Workloads > Secrets** section on your {{site.data.keyword.redhat_openshift_notm}} cluster. Search for `<instance_id>-credentials-superuser name` under **Secrets** section. For example, if you entered `inst1` as input value to **mas_instance_id input** field then search for `inst1-credentials-superuser name` under **Secrets** section.
     {: note}

    If the deployment fails, the process is exited. You can find the reason for failure in the schematics log.

For information about accessing the {{site.data.keyword.prodname_imas_short}}, see [Getting started](https://www.ibm.com/docs/en/mas-cd/continuous-delivery?topic=getting-started){: external}.
