---

copyright:
  years: 2024
lastupdated: "2024-04-24"

keywords: accessing, maximo application suite, deployable architecture, suite administrator

subcollection: maximo-application-suite

---


{{site.data.keyword.attribute-definition-list}}

# Deploying {{site.data.keyword.redhat_openshift_notm}} Kubernetes Service VPC cluster
{: #deploy-redhat-openshift-kubernetes-service}

You can deploy a {{site.data.keyword.redhat_openshift_notm}} Kubernetes Service VPC (Gen2 infrastructure) cluster using {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone DA from {{site.data.keyword.cloud_notm}} Public Catalog.
{: shortdesc}

1. Go to {{site.data.keyword.cloud_notm}} public catalog and search for {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone DA and click on it's tile.
1. Select the Product version. Select **Variation** as Standard and click **Add to project**.
1. On **Add to project** page, either create a project or add to your existing project.
   - To create a project, enter Name, Description (optional), select a Region, and Resource group
   - To add to existing project, select option, project, and enter either a new configuration name or use the default configuration name. Click **Add**.
1. On **Edit configuration** page, under **Configure > Security** section, enter your api_key by either selecting from **Secrets Manager** or by entering it manually.
   If you are using the Secrets Mananger, ensure you have granted required permissions and created the API key. For more information, see [Using an API key with secrets manager to authorize a project to deploy an architecure](/docs/secure-enterprise?topic=secure-enterprise-authorize-project).
1. Under **Required** section, select `kube_version` as `4.12_openshift`. Select the region where you are planning to create this cluster. For prefix field, enter a unique name.
1. Under **Optional** section, click the edit option in front of `override_json_string` field and in the pop-up window, remove the double quotes ("") and enter the content that is provided in the `override.json` file and click **Save** button.
    - For information about an example on different deployment options, see the [override.json](https://github.com/terraform-ibm-modules/terraform-ibm-landing-zone/blob/main/examples/override-example/override.json){: external} file.
    - For more information about {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone deployment architecture, see [Overview](https://cloud.ibm.com/docs/secure-infrastructure-vpc?topic=secure-infrastructure-vpc-overview).
1. If you have entered all required values then **Validate** button will be visible. Click it.
1. The validation starts and on **Vaidation changes** page, you can see a message > All changes are scanned for code errors, cost, and compliance. and it's generating plan. These activities can take time to complete.
1. Make sure validation completes and it displays Validation successful message.
1. On Approval pending section, enter `I approve` and click **Approve** button.
1. Click **Deploy** option. This will start deploying of the cluster.
