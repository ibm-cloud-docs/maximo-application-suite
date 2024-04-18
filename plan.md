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

## Preparing to install Maximo Application Suite using MAS DA from IBM Cloud Public Catalog
{: ##preparing}

Before you install IBM® Maximo® Application Suite or Maximo Application Suite Core + Manage, consider your installation preferences such as the type of Maximo Application Suite offering that you prefer.
The following offering types are supported:

1) MAS Core
2) MAS Core + Manage (with internal DB2 deployed on {{site.data.keyword.redhat_openshift_full}} cluster)

## Prerequisites
{: ##prerequisites}

Before you install Maximo Application Suite Core or Maximo Application Suite Core + Manage, you must complete several tasks, such as creating an {{site.data.keyword.redhat_openshift_short}} cluster,
obtaining an {{site.data.keyword.Bluemix_short}} Entitled Registry key, {{site.data.keyword.Bluemix_short}} API Key, Maximo Application Suite License file, SLS license ID.

### {{site.data.keyword.redhat_openshift_short}} Cluster
{: ###openshiftcluster}

You should already have a target {{site.data.keyword.redhat_openshift_short}} cluster ready to install Maximo Application suite into.
If you do not already have one then install it using {{site.data.keyword.redhat_openshift_short}} Deployable Architecture available on {{site.data.keyword.Bluemix_short}} public catalog or
refer to the {{site.data.keyword.redhat_openshift_short}} Container Platform installation overview.

### {{site.data.keyword.Bluemix_short}} Entitled Registry key
{: ###entitledregkey}

To access your software in the entitled registry, obtain an {{site.data.keyword.Bluemix_short}} Entitled Registry key. (<https://myibm.ibm.com/products-services/containerlibrary>)

### Maximo Application Suite license
{: ###maslic}

The Maximo Application Suite license needs to be retrieved from the {{site.data.keyword.IBM_short}} License Key Center.
If you do not already have your Maximo Application Suite license key file, you can create and download it in the {{site.data.keyword.Bluemix_short}} License Key Center. (<https://licensing.subscribenet.com/control/ibmr/login>)

### Maximo Application Suite license ID
{: ###maslicid}

A unique 12-character hexadecimal value, such as `0abcac110f02` in the first line of your Maximo Application Suite license key file.

### {{site.data.keyword.Bluemix_short}} API Key
{: ###cloudapikey}

Your {{site.data.keyword.Bluemix_short}} Cloud account's API key. If you do not have it, see
<https://cloud.ibm.com/docs/account?topic=account-userapikey&interface=ui>
