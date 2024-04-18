---

copyright:
  years: 2024
lastupdated: "2024-04-17"

keywords:

subcollection: maximo-application-suite

---

# Planning for Maximo Application Suite deployable architecture
{: #planning}

Use this topic if you have prerequisites, dependencies, or other information a customer needs to be able to quickly deploy this architecture from the catalog into a project.
{: shortdesc}

## Preparing to install Maximo Application Suite by using deployable architecture from {{site.data.keyword.Bluemix_full}} Public catalog
{: ##preparing}

Before you install IBM® Maximo® Application Suite or Maximo Application Suite Core + Manage, consider your installation preferences such as the type of Maximo Application Suite offering that you prefer.
The following offering types are supported:

1) MAS Core
2) MAS Core + Manage (with internal Db2 deployed on {{site.data.keyword.redhat_openshift_full}} cluster)

## Prerequisites
{: ##prerequisites}

Before you install Maximo Application Suite Core or Maximo Application Suite Core + Manage, you must complete several tasks.

1) Creating an {{site.data.keyword.redhat_openshift_notm}} cluster
2) Obtaining an {{site.data.keyword.Bluemix_notm}} Entitled Registry key
3) {{site.data.keyword.Bluemix_notm}} API Key
4) Maximo Application Suite license file
5) SLS license ID

### {{site.data.keyword.redhat_openshift_notm}} Cluster
{: ###openshiftcluster}

You must have a target {{site.data.keyword.redhat_openshift_notm}} cluster ready to install Maximo Application Suite into.
If you do not already have one, then install it using {{site.data.keyword.redhat_openshift_notm}} Deployable Architecture available on {{site.data.keyword.Bluemix_short}} public catalog or
refer to the {{site.data.keyword.redhat_openshift_notm}} Container Platform installation overview.

### {{site.data.keyword.Bluemix_short}} Entitled Registry key
{: ###entitledregkey}

To access your software in the entitled registry, obtain an {{site.data.keyword.Bluemix_short}} Entitled Registry key. For more information, see [Entitlement keys](<https://myibm.ibm.com/products-services/containerlibrary>.)

### Maximo Application Suite license
{: ###maslic}

The Maximo Application Suite license needs to be retrieved from the {{site.data.keyword.IBM_short}} License Key Center.
If you do not already have your Maximo Application Suite license key file, you can create and download it in the {{site.data.keyword.Bluemix_short}} License Key Center. For more information, see [how to request specific license keys for IBM software products](<https://licensing.subscribenet.com/control/ibmr/login>.)

### Maximo Application Suite license ID
{: ###maslicid}

A unique 12-character hexadecimal value, such as `0abcac110f02` in the first line of your Maximo Application Suite license key file.

### {{site.data.keyword.Bluemix_short}} API Key
{: ###cloudapikey}

Your {{site.data.keyword.Bluemix_short}} Cloud account's API key. If you do not have it, see
[Managing user API keys](<https://cloud.ibm.com/docs/account?topic=account-userapikey&interface=ui>.)
