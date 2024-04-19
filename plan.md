---

copyright:
  years: 2024
lastupdated: "2024-04-17"

keywords:

subcollection: maximo-application-suite

---

{{site.data.keyword.attribute-definition-list}}

# Planning for Maximo Application Suite deployable architecture
{: #planning}

Before you install IBM® Maximo® Application Suite or Maximo Application Suite Core + Maximo Manage, consider your installation preferences such as the type of Maximo Application Suite offering that you prefer.
{: shortdesc}

The following offering types are supported:

1. Maximo Application Suite Core
1. Maximo Application Suite Core + Maximo Manage

Maximo Application Suite Core is deployed by using the MongoDB Community edition and Maximo Manage is deployed with internal Db2 on {{site.data.keyword.redhat_openshift_full}} cluster.
{: note}

## Prerequisites
{: #prerequisites}

Before you install Maximo Application Suite Core or Maximo Application Suite Core + Manage, you must complete the following tasks.

1. Create an {{site.data.keyword.redhat_openshift_notm}} cluster
1. Obtain an {{site.data.keyword.Bluemix_notm}} Entitled Registry key
1. Retrieve the {{site.data.keyword.Bluemix_notm}} API Key
1. Get the Maximo Application Suite license file
1. Retireve the SLS license ID

### {{site.data.keyword.redhat_openshift_notm}} Cluster
{: #openshiftcluster}

You must have a target {{site.data.keyword.redhat_openshift_notm}} cluster ready to install Maximo Application Suite into.
If you do not already have one, then install it using {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone available on {{site.data.keyword.Bluemix_short}} public catalog or
refer to the {{site.data.keyword.redhat_openshift_notm}} Container Platform installation overview.

### {{site.data.keyword.Bluemix_short}} Entitled Registry key
{: #entitledregkey}

To access your software in the entitled registry, obtain an {{site.data.keyword.Bluemix_short}} Entitled Registry key.

For more information, see [Entitlement keys](https://myibm.ibm.com/products-services/containerlibrary){: external}.

### Maximo Application Suite license
{: #maslic}

The Maximo Application Suite license needs to be retrieved from the {{site.data.keyword.IBM_short}} License Key Center.
If you do not already have your Maximo Application Suite license key file, you can create and download it in the {{site.data.keyword.Bluemix_short}} License Key Center.

For more information, see [how to request specific license keys for IBM software products](https://licensing.subscribenet.com/control/ibmr/login){: external}.

### Maximo Application Suite license ID
{: #maslicid}

A unique 12-character hexadecimal value, such as `0abcac110f02` in the first line of your Maximo Application Suite license key file.

### {{site.data.keyword.Bluemix_short}} API Key
{: #cloudapikey}

Your {{site.data.keyword.Bluemix_short}} Cloud account's API key. If you do not have it, see
[Managing user API keys](/docs/account?topic=account-userapikey&interface=ui).
