---

copyright:
  years: 2024
lastupdated: "2024-04-17"

keywords: deployable architecure, maximo application suite

subcollection: maximo-application-suite

---

{{site.data.keyword.attribute-definition-list}}

# Planning for {{site.data.keyword.prodname_imas_short}} deployable architecture
{: #planning}

Before you install {{site.data.keyword.prodname_imas_full}} or {{site.data.keyword.prodname_imas_short}} Core + {{site.data.keyword.IBM}} Maximo Manage, consider your installation preferences such as the type of {{site.data.keyword.prodname_imas_short}} offering that you prefer.
{: shortdesc}

The following offering types are supported:

1. {{site.data.keyword.prodname_imas_short}} Core
1. {{site.data.keyword.prodname_imas_short}} Core + Maximo Manage

{{site.data.keyword.prodname_imas_short}} Core is deployed by using the MongoDB Community edition and Maximo Manage is deployed with internal Db2 on {{site.data.keyword.redhat_openshift_full}} cluster.
{: note}

## Prerequisites
{: #prerequisites}

Before you install {{site.data.keyword.prodname_imas_short}} Core or {{site.data.keyword.prodname_imas_short}} Core + Manage, you must complete the following tasks.

1. Create an {{site.data.keyword.redhat_openshift_notm}} cluster
1. Obtain an {{site.data.keyword.cloud}} Entitled Registry key
1. Retrieve the {{site.data.keyword.cloud_notm}} API Key
1. Get the {{site.data.keyword.prodname_imas_short}} license file
1. Retireve the SLS license ID

### {{site.data.keyword.redhat_openshift_notm}} Cluster
{: #openshiftcluster}

You must have a target {{site.data.keyword.redhat_openshift_notm}} cluster ready to install {{site.data.keyword.prodname_imas_short}}.
If you do not already have one, then install it using {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone available on {{site.data.keyword.cloud_notm}} public catalog or
refer to the {{site.data.keyword.redhat_openshift_notm}} Container Platform installation overview.
Make sure your existing {{site.data.keyword.redhat_openshift_notm}} cluster has outbound access to 'quay.io' registry site.

For example, follow these steps to deploy a ROKS VPC (Gen2 infrastructure) cluster using {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone DA from {{site.data.keyword.cloud_notm}} Public Catalog.

1. Go to {{site.data.keyword.cloud_notm}} public catalog and search for {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone DA and click on it's tile.
1. Select the Product version. Select **Variation** as Standard and click **Add to project**.
1. On **Add to project** page, either create a project or add to your existing project.
 - To create a project, enter Name, Description (optional), select a Region, and Resource group
 - To add to existing project, select option, project, and enter either a new configuration name or use the default configuration name. Click **Add**.
1. On **Edit configuration** page, under **Configure > Security** section, enter your api_key by either selecting from **Secrets Manager** or by entering it manually.
1. Under **Required** section, select kube_version as 4.12_openshift. Select the region where you are planning to create this cluster. For prefix field, enter a unique name.
1. Under **Optional** section, click the edit option in front of override_json_string field and in the pop-up window, remove the double quotes ("") and enter the content that is provided in the attached 'override.json' file and click **Save** button.

For more information about {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone DA, see https://cloud.ibm.com/docs/secure-infrastructure-vpc?topic=secure-infrastructure-vpc-overview.
For information about an example on different deployment option and override.json file, see https://github.com/terraform-ibm-modules/terraform-ibm-landing-zone/blob/main/examples/override-example/override.json

1. If you have entered all required values then Validate button will be visible at the top right corner of the page. Click on it.
1. The validation starts and on Vaidation changes page, you can see a message "All changes are scanned for code errors, cost, and compliance." and it's generating plan. These activities can take up few minutes.
1. Make sure validation completes and it displays Validation successful message.
1. On Approval pending section, enter "I approve" and click on Approve button.
1. Click on Deploy option. This will start deploying of the cluster.

### {{site.data.keyword.cloud_notm}} Entitled Registry key
{: #entitledregkey}

To access your software in the entitled registry, obtain an {{site.data.keyword.cloud_notm}} Entitled Registry key.

For more information, see [Entitlement keys](https://myibm.ibm.com/products-services/containerlibrary){: external}.

### {{site.data.keyword.prodname_imas_short}} license
{: #maslic}

The {{site.data.keyword.prodname_imas_short}} license needs to be retrieved from the {{site.data.keyword.IBM}} License Key Center.
If you do not already have your {{site.data.keyword.prodname_imas_short}} license key file, you can create and download it in the {{site.data.keyword.cloud_notm}} License Key Center.

For more information, see [how to request specific license keys for IBM software products](https://licensing.subscribenet.com/control/ibmr/login){: external}.

### {{site.data.keyword.prodname_imas_short}} license ID
{: #maslicid}

A unique 12-character hexadecimal value, such as `0abcac110f02` in the first line of your {{site.data.keyword.prodname_imas_short}} license key file.

### {{site.data.keyword.cloud_notm}} API Key
{: #cloudapikey}

Your {{site.data.keyword.cloud_notm}} account's API key. If you do not have it, see
[Managing user API keys](/docs/account?topic=account-userapikey&interface=ui).
