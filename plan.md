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

Before you install {{site.data.keyword.prodname_imas_full}} or {{site.data.keyword.prodname_imas_short}} Core + {{site.data.keyword.prodname_IBM}} Maximo Manage, consider your installation preferences such as the type of {{site.data.keyword.prodname_imas_short}} offering that you prefer.
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

### {{site.data.keyword.cloud_notm}} Entitled Registry key
{: #entitledregkey}

To access your software in the entitled registry, obtain an {{site.data.keyword.cloud_notm}} Entitled Registry key.

For more information, see [Entitlement keys](https://myibm.ibm.com/products-services/containerlibrary){: external}.

### {{site.data.keyword.prodname_imas_short}} license
{: #maslic}

The {{site.data.keyword.prodname_imas_short}} license needs to be retrieved from the {{site.data.keyword.IBM_short}} License Key Center.
If you do not already have your {{site.data.keyword.prodname_imas_short}} license key file, you can create and download it in the {{site.data.keyword.cloud_notm}} License Key Center.

For more information, see [how to request specific license keys for IBM software products](https://licensing.subscribenet.com/control/ibmr/login){: external}.

### {{site.data.keyword.prodname_imas_short}} license ID
{: #maslicid}

A unique 12-character hexadecimal value, such as `0abcac110f02` in the first line of your {{site.data.keyword.prodname_imas_short}} license key file.

### {{site.data.keyword.cloud_notm}} API Key
{: #cloudapikey}

Your {{site.data.keyword.cloud_notm}} account's API key. If you do not have it, see
[Managing user API keys](/docs/account?topic=account-userapikey&interface=ui).
