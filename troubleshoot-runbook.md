---

copyright:
  years: 2024
lastupdated: "2024-04-26"

keywords: question about _xx_, _messageID_

subcollection: maximo-application-suite

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# How do I address a failed cluster configuration download?
{: #ts-failed-cluster-config-download}
{: troubleshoot}


When you try to download the cluster configuration, you get an error.
{: shortdesc}

You see the following error messages when you try to download a cluster configuration:
{: tsSymptoms}

## Error downloading the cluster config
{: #download-error}

In schematic logs, you see the following error entry:

```htm
Terraform plan | Error: [ERROR] Error downloading the cluster config [masdaapr24-management-cluster]: Request failed with status code: 404, ServerErrorResponse: {"incidentID":"9b8fd6b3-bd93-4449-90df-1f28ef7ff303","code":"G0004","description":"The specified cluster could not be found. If applicable, make sure that you target the correct account and resource group.","type":"General","recoveryCLI":"To list the clusters you have access to, run 'ibmcloud ks cluster ls'. To list the resource groups that you have access to, run 'ibmcloud resource groups'. To target the resource group, run 'ibmcloud target -g \u003cresource_group\u003e'."}
Terraform plan |
Terraform plan | with data.ibm_container_cluster_config.cluster_config,
Terraform plan | 1: data "ibm_container_cluster_config" "cluster_config" {
Terraform plan error: Terraform PLAN errorexit status 1
```

This error indicates that either the existing cluster id that you entered is incorrect or there is no ingress connection enabled for this cluster.
{: tsCauses}

## Invalid value for variable deployment_flavor
{: #invalid-value-error}

```htm
In schematic logs, you can see the following error entry:
Terraform plan | variable "deployment_flavor" {
Terraform plan |     ├────────────────
Terraform plan |     │ var.deployment_flavor is "core2"
Terraform plan |
Terraform plan | Invalid deployment flavor type! Valid values are 'core' or 'manage'
```

This error indicates that the value for deployment_flavor that you entered is other than core or manage. Make sure you enter these values in lower-case without any quotes.
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

Add run book
{: tsResolve}
