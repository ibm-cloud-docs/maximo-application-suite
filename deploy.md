---

copyright:
  years: 2024
lastupdated: "2024-04-17"

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
1. Make sure that you comply with the prerequisites in the [planning](/docs/maximo-application-suite?topic=maximo-application-suite-planning) topic:
 - Have an {{site.data.keyword.cloud_notm}} API key.
 - Verify access roles.
 - Create an SSH key.

1. Go to the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog#reference_architecture){: external} and search for the architecture that you are interested in deploying.

1. Click the tile for the deployable architecture to open the details.

1. Select the latest product version in the Architecture section.

1. Select a variation, if more than one is available.

1. Click **Review deployment options**.

1. Select the **Add to project** deployment type in Deployment options, and then click **Add to project**.
 - Name your project, enter a description, and specify a configuration name. Click Create.
1. Edit and validate the configuration:
 - Select your authentication method. You can use an existing secret in Secrets Manager or add your API key directly. For more information, see [Using an API key or secret to authorize projects](/docs/secure-enterprise?topic=secure-enterprise-authorize-project).
 - Enter values for other required fields from the Required tab.
 - Optional: Specify other values from the Optional tab.
 - Save the configuration.
 - Click **Validate**. Validation takes a few minutes

{{site.data.keyword.cloud_notm}} projects runs a Code Risk Analyzer scan that includes a [supported set of Security and Compliance Center rules](/docs/code-risk-analyzer-cli-plugin?topic=code-risk-analyzer-cli-plugin-cra-cli-plugin#terraform-scc-rules). Controls that are part of the deployable architecture and that are also supported by {{site.data.keyword.cloud_notm}} projects are checked. Any extra controls that are not included in the list of supported Security and Compliance Center rules are not checked when you validate the configuration.
If the validation fails because of the Code Risk Analyzer scan, you can [troubleshoot the failure](/docs/maximo-application-suite?topic=maximo-application-suite-troubleshoot-mas-da-failed-validation).

1. Deploy the configuration:

After you validate your configuration, you can deploy it to your target account.
 - Review the input values and make any necessary changes.
 - Click **Deploy**.

Deploying the deployable architecture can take more than an hour. You are notified when the deployment is successful.

1. Review the outputs from the deployable architecture.

During the validation and deployment process, monitor the [needs attention items](https://cloud.ibm.com/docs/secure-enterprise?topic=secure-enterprise-needs-attention-projects). The widget reflects any issue that occurs in your configurations.
{: remember}

<!-- if part of deploying you have nuances to call out do this in this topic. think gotchas, connections as part of deploying, etc. Do you have an override or other complex scenarios to call out? -->
