---

copyright:
  years: 2024
lastupdated: "2024-04-17"

keywords: question about _xx_, _messageID_

subcollection: maximo-application-suite

content-type: troubleshoot

---

<!-- keywords values above are place holders. Actual values should be pulled from the Troubleshooting questions or error message to which the issue relates. Only use a messageID if the troubleshooting topic is about an issue encountered from an error message that has an ID.  -->

{{site.data.keyword.attribute-definition-list}}

<!-- You must add the troubleshoot content type in your attribute definitions AND on a new line under each troubleshooting topic H1 ID. This will ensure that the troubleshooting entry is pulled into other locations, like chatbots. Use the support attribute definition for reuse in the support center. For more information, see  https://test.cloud.ibm.com/docs/writing?topic=writing-support-center#support-center-troubleshoot-->

<!-- Remember that this is the individual topic template for each troubleshooting entry that belongs in a troubleshooting topic group in the Help left nav group. For more information, see the guidance page: https://test.cloud.ibm.com/docs/writing?topic=writing-troubleshooting-topics-->

# How do I address a failed validation when using projects?
{: #troubleshoot-mas-da-failed-validation}
{: troubleshoot}

 <!-- {: support} Only add this attribute to entries that you want to display in the support center. -->

<!--The title of your H1 should be a problem statement in question format of the issue that the user is experiencing. Think about the user's language they might use to describe or search for the answer to the issue they are experiencing. Use keywords for other variations of ways to ask the question at the top of the file. -->

When you try to download the cluster configuration, you get an error.
{: shortdesc}

You see the following error messages when you try to download a cluster configuration:
{: tsSymptoms}

## Error downloading the cluster config
{: #download-error}

In schematic logs, you see the following error entry:
````Terraform plan | Error: [ERROR] Error downloading the cluster config [masdaapr24-management-cluster]: Request failed with status code: 404, ServerErrorResponse: {"incidentID":"9b8fd6b3-bd93-4449-90df-1f28ef7ff303","code":"G0004","description":"The specified cluster could not be found. If applicable, make sure that you target the correct account and resource group.","type":"General","recoveryCLI":"To list the clusters you have access to, run 'ibmcloud ks cluster ls'. To list the resource groups that you have access to, run 'ibmcloud resource groups'. To target the resource group, run 'ibmcloud target -g \u003cresource_group\u003e'."}
Terraform plan |
Terraform plan |   with data.ibm_container_cluster_config.cluster_config,
Terraform plan |    1: data "ibm_container_cluster_config" "cluster_config" {
Terraform plan error: Terraform PLAN errorexit status 1

````
{: codeblock}

This error indicates that either the existing cluster id that you entered is incorrect or there is no ingress connection enabled for this cluster.
{: tsCauses}

## Invalid value for variable deployment_flavour
{: #invalid-value-error}

In schematic logs, you can see the following error entry:
````Terraform plan |     variable "deployment_flavour" {
Terraform plan |     ├────────────────
Terraform plan |     │ var.deployment_flavour is "core2"
Terraform plan |
Terraform plan | Invalid deployment flavour type! Valid values are 'core' or 'manage'
````
{: codeblock}

This error indicates that the value for deployment_flavour that you entered is other than core or manage. Make sure you enter these values in lower case without any quotes.
{: tsCauses}

## Other validation errors
{: #other-errors}

If the validation failed, it likely means that a required input value, such as an authentication method, has not been supplied yet or one of the provided inputs is not valid.

Deployment will fail if one of the provided inputs is not valid. Check the output message for pipeline_execution_status and if it is not a message about sucess, then it means that the deployment has failed.

If deployment has failed then it will capture the tekton install pipeline task which has failed and it will output the failed task information in the pipeline_execution_status output field. Check the log of failed task by logging into your existing {{site.data.keyword.redhat_openshift_full}} cluster and then by navigating to **Pipelines > Pipelines** and
then by clicking on the installation pipeline and checking the log file of failed task for further information.

There could be several reasons for deployment to fail.
For example, if an invalid license file is entered, then it will show the following message:
License key file is missing required MAS product features in the pipeline task log.

Other examples are, if incorrect or non-existing storage class is entered.
If file storage class is not entered then internal DB2 installation will fail.
Deployment will also fail if you try to create the same {{site.data.keyword.prodname_imas_full}} instance on your {{site.data.keyword.redhat_openshift_notm}} cluster by passing the existing {{site.data.keyword.prodname_imas_short}} instance Id value to **input variable > mas_instance_id**.
{: codeph}
