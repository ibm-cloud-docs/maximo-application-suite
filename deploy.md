---

copyright:
  years: 2024
lastupdated: "2024-12-02"

keywords:

subcollection: maximo-application-suite

---


{{site.data.keyword.attribute-definition-list}}

# Deploying or uninstalling {{site.data.keyword.prodname_imas_short}} deployable architecture
{: #deploying-da}

You can deploy or remove a deployable architecture from the {{site.data.keyword.cloud_notm}} catalog. You can choose among different deployment options, including with {{site.data.keyword.cloud_notm}} projects.
{: shortdesc}

- [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

## Deploying with {{site.data.keyword.cloud_notm}} projects
{: #maximo-application-suite-deploy-cloud}

To deploy the {{site.data.keyword.prodname_imas_full}} Deployable Architecture (DA) through the {{site.data.keyword.cloud_notm}} catalog, follow these steps:

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

       You are notified when the deployment is complete and with successful or failure message. If it fails, refer to the schematics log.
1. Review the outputs from the deployable architecture.
   - **maximo_admin_url** : The admin URL to the deployed offering is displayed here.
       Login credentials to this admin url can be found under the **Workloads > Secrets** section on your {{site.data.keyword.redhat_openshift_notm}} cluster. Search for `<instance_id>-credentials-superuser name` in **Secrets** section.

       For example, if you entered `inst1` as input value to **mas_instance_id input** field then search for `inst1-credentials-superuser name` in **Secrets** section.
       {: note}

       If the deployment fails, the process is exited. You can find the reason for failure in the schematics log.

       After you uninstall the application, some persistent volumes remain. You can choose to either retain or manually remove the data.
       {: tip}

- For information about accessing {{site.data.keyword.prodname_imas_short}}, see [Getting started](https://www.ibm.com/docs/en/masv-and-l/continuous-delivery?topic=getting-started){: external}.

## Upgrading or updating with {{site.data.keyword.prodname_imas_short}} Deployable Architecture
{: #upgrading-or-updating-maximo-application-suite}


 - {{site.data.keyword.cloud_notm}} Projects

    Deploy a new instance of {{site.data.keyword.prodname_imas_short}} 9.0.3 using {{site.data.keyword.prodname_imas_short}} Deployable Architecture (DA) version 2.0.1 from the {{site.data.keyword.cloud_notm}} Projects page. For more information, see [Deploying with {{site.data.keyword.cloud_notm}} projects](/docs/maximo-application-suite?topic=maximo-application-suite-deploying-da#maximo-application-suite-deploy-cloud) section.

    If you have previously deployed a {{site.data.keyword.prodname_imas_short}} instance using the now deprecated DA version 1.7.5, you must first remove the deployment and then deploy a new {{site.data.keyword.prodname_imas_short}} instance. Do not deploy {{site.data.keyword.prodname_imas_short}} directly with DA version 2.0.1 from the {{site.data.keyword.cloud_notm}} **Projects** page as rolling back to the previous DA version is not supported.
    {: note}

    To remove the previous {{site.data.keyword.prodname_imas_short}} instance, follow the steps that are given in [Uninstalling with {{site.data.keyword.cloud_notm}} projects](/docs/maximo-application-suite?topic=maximo-application-suite-deploying-da#undeploy) section.

 - {{site.data.keyword.prodname_imas_short}} command line utility

    Use the {{site.data.keyword.prodname_imas_short}} command line utility to deploy a {{site.data.keyword.prodname_imas_short}} instance. For more information, see [Upgrade procedure](https://ibm-mas.github.io/cli/guides/upgrade/){: external}.



## Uninstalling with {{site.data.keyword.cloud_notm}} projects
{: #undeploy}

1. To remove the previous {{site.data.keyword.prodname_imas_short}} DA version, from the **Projects** page, select the project where you created the previous {{site.data.keyword.prodname_imas_short}} DA version.
1. In the **Configurations** tab, select the {{site.data.keyword.prodname_imas_short}} DA configuration.
1. Click the **Undeploy** option.
1. On the **Undeploy configuration** dialog, enter the configuration name.
1. Click **Undeploy**.

    This action uninstalls the previous {{site.data.keyword.prodname_imas_short}} DA version from your cluster and removes the resources that are created by it.

    You can view the uninstallation log on the Schematics workspace. Simultaneously, you can view the uninstall tekton pipeline that is created on your cluster console.

After you uninstall the application, some persistent volumes remain. You can choose to either retain or manually remove the data.
{: tip}

Make sure that the uninstall is successful before you reinstall the same or new DA version.
{: note}
