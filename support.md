---

copyright:
  years: 2024
lastupdated: "2024-04-17"

keywords:

subcollection: maximo-application-suite

---

{{site.data.keyword.attribute-definition-list}}

<!-- Use your deployable architecture  name in the title to help search results, and use a nav title in the toc.yaml to shorten it to Getting help and support in the left nav-->

# Getting help and support for {{site.data.keyword.prodname_imas_short}}
{: #help-and-support}

If you experience an issue or have questions when deploying {{site.data.keyword.prodname_imas_short}}, you can use the following resources before you open a support case.
{: shortdesc}

* Review the [FAQs](/docs/sap-powervs?topic=sap-powervs-faqs) in the deployment guide.
* Review the [troubleshooting documentation](/docs/sap-powervs?topic=sap-powervs-troubleshoot) to troubleshoot and resolve common issues.
* ![IBM Cloud icon](images/ibm-cloud-16.svg "IBM Cloud icon") Check the status of the {{site.data.keyword.cloud_notm}} platform and resources by going to the [Status page](https://cloud.ibm.com/status){: external}.
* ![GitHub icon](../icons/logo-github-16.svg "GitHub icon") Review the [GitHub issues](https://github.com/terraform-ibm-modules/terraform-ibm-powervs-sap/issues){: external} to see whether other users experienced the same problem.


<!-- In this list above, you can also provide a public slack channel for searching for answers or asking questions in a forum, if there is one available. For example, you'd include a bullet like "![Slack icon](../icons/logo-slack-16.svg "GitHub icon") Ask product experts and the community questions on the [slack-channel-name)[url.com] slack channel."  -->

If you still can't resolve the problem, you can open a support case. For more information, see [Creating support cases](/docs/get-support?topic=get-support-open-case). And, if you're looking to provide feedback, see [Submitting feedback](/docs/overview?topic=overview-feedback).

## Providing support case details
{: #support-case-details}

To ensure that the support team can start investigating your case to provide a timely resolution, you must include details from two logs from your failed deployment.


1. From your Schematics log, provide the architecture name, source URL, and version.
   a. In the {{site.data.keyword.cloud_notm}} console, go to **Schematics** > **Workspaces** > **deployable architecture instance**.
   b. Copy and paste into the case details the portion of the log that provides the architecture information. The following is an example of what should be copied:

      ```sh
      2023/04/06 18:11:43 Related Workspace: name=deploy-arch-ibm-slz-ocp-04-06-2023, sourcerelease=(not specified), sourceurl=https modules/terraform-ibm-landing-zone/archive/v3.1.2.tar.gz,tolder=terratorm-ibm-landing-zone-3.1.2/patterns/roks
       ```

2. Provide the Terraform Log Analyzer summary from your project.
   a. In the {{site.data.keyword.cloud_notm}} console, go to **your project** > **Configurations** > **deployable architecture instance**.
   b. Depending on where you are in your deployment process go to **Viewing validation results** or **Viewing last deployment**. Take a screenshot of the results and add it to your support case.

## Routing your support case expeditiously
{: #support-case-routing}

To get your support case routed correctly to speed up resolution, make sure that you select the right product when you open the case.

If you're having issues getting the deployable architecture deployed, use the name of the deployable architecture as it is listed in the catalog.

However, if you successfully deployed and are instead having an issue with a service in the deployable architecture, set that service as the product name in the case.
