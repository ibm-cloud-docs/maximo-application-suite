---

copyright:
  years: 2024
lastupdated: "2024-04-17"

keywords:

subcollection: maximo-application-suite

---

{{site.data.keyword.attribute-definition-list}}

# Getting help and support for {{site.data.keyword.prodname_imas_short}}
{: #help-and-support}

If you experience an issue or have questions when you deploy {{site.data.keyword.prodname_imas_short}}, you can use the following resources before you open a support case.
{: shortdesc}

* Review the [FAQs](/docs/maximo-application-suite?topic=maximo-application-suite-faqs) in the deployment guide.
* Review the [troubleshooting documentation](/docs/maximo-application-suite?topic=maximo-application-suite-ts-na-failures) to troubleshoot and resolve common issues.
* Check the status of the {{site.data.keyword.cloud_notm}} platform and resources by going to the [Status page](https://cloud.ibm.com/status){: external}.
* Review the [GitHub issues](https://github.com/terraform-ibm-modules/terraform-ibm-mas){: external} to see whether other users experienced the same problem.

If you still can't resolve the problem, you can open a support case with the Maximo support team. For more information, see [Creating support cases](https://www.ibm.com/mysupport/s/topic/0TO0z000000Zas8GAC/maximo-application-suite). And, if you're looking to provide feedback, see [Submitting feedback](/docs/overview?topic=overview-feedback).

## Providing support case details
{: #support-case-details}

To ensure that the support team can start investigating your case to provide a timely resolution, you must include details from two logs from your failed deployment.


1. From your Schematics log, provide the architecture name, source URL, and version.
   a. In the {{site.data.keyword.cloud_notm}} console, go to **Schematics** > **Workspaces** > **deployable architecture instance**.
   b. Copy and paste into the case details the portion of the log that provides the architecture information. The following code is an example of what can be copied:

      ```sh
      2023/04/06 18:11:43 Related Workspace: name=deploy-arch-ibm-slz-ocp-04-06-2023, sourcerelease=(not specified), sourceurl=https modules/terraform-ibm-landing-zone/archive/v3.1.2.tar.gz,tolder=terratorm-ibm-landing-zone-3.1.2/patterns/roks
       ```

2. Provide the Terraform Log Analyzer summary from your project.
   a. In the {{site.data.keyword.cloud_notm}} console, go to **your project** > **Configurations** > **deployable architecture instance**.
   b. Depending on where you are in your deployment process go to **Viewing validation results** or **Viewing last deployment**. Take a screenshot of the results and add it to your support case.

## Routing your support case expeditiously
{: #support-case-routing}

To get your support case routed correctly to speed up resolution, make sure that you select the correct product when you open the case.

If you are having issues with deploying the deployable architecture, identify in the case description that you are using the {{site.data.keyword.prodname_imas_short}} deployable architecture on {{site.data.keyword.cloud_notm}}.

If you successfully deployed and are instead having an issue with the {{site.data.keyword.prodname_imas_short}} software itself, use the same route to engage the Maximo Support team and identify the Suite applications that are deployed.
