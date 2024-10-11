---

copyright:
  years: 2024
lastupdated: "2024-10-11"

keywords: deployable architecture, maximo application suite

subcollection: maximo-application-suite

content-type: release-note

---

{{site.data.keyword.attribute-definition-list}}

# Release notes for {{site.data.keyword.prodname_imas_short}} Deployable Architecture
{: #release-notes}

Use these release notes to learn about the latest updates to {{site.data.keyword.prodname_imas_full}} Deployable Architecture that are grouped by month. Release notes are available for a minimum of three years.
{: shortdesc}

## October 2024
{: #october-release}

- Introducing {{site.data.keyword.prodname_imas_short}} Deployable Architecture 2.0.1

   You can now deploy a {{site.data.keyword.prodname_imas_short}} 9.0.3 instance using {{site.data.keyword.prodname_imas_short}} Deployable Architecture (DA) version 2.0.1 from the {{site.data.keyword.cloud_notm}} **Projects** page or {{site.data.keyword.prodname_imas_short}} command line utility.

   If you have previously deployed a {{site.data.keyword.prodname_imas_short}} instance using the now deprecated DA version 1.7.5, you must first remove the deployment. Do not deploy {{site.data.keyword.prodname_imas_short}} instance directly with DA version 2.0.1 as rolling back to the previous DA version is not supported.
   {: note}

   For more information, see [Deploying {{site.data.keyword.prodname_imas_short}} deployable architecture](/docs/maximo-application-suite?topic=maximo-application-suite-deploying-da#upgrading-or-updating-maximo-application-suite).

- Support for {{site.data.keyword.redhat_openshift_notm}} Container Platform 4.15.x

   Enable the outbound traffic on your cluster to use the {{site.data.keyword.redhat_openshift_notm}} Container Platform 4.15.x that is available from the {{site.data.keyword.redhat_openshift_notm}} landing zone DA.

   For more information, see [Deploying {{site.data.keyword.redhat_openshift_notm}} Kubernetes Service](/docs/maximo-application-suite?topic=maximo-application-suite-deploy-redhat-openshift-kubernetes-service) and [{{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone](https://cloud.ibm.com/catalog/architecture/deploy-arch-ibm-slz-ocp-95fccffc-ae3b-42df-b6d9-80be5914d852-global){: external}.

- Faster deployment with `ibmc-vpc-file-500-iops` storage class

   By default, `storage_class_rwx` is updated to the faster `ibmc-vpc-file-500-iops` storage class. Therefore, use the `vpc-file-csi-driver` addon version 2.0 that includes this storage class.

## April 2024
{: #aprilrelease}

- Introducing {{site.data.keyword.prodname_imas_short}} Deployable Architecture

   You can now deploy {{site.data.keyword.prodname_imas_short}} Core or {{site.data.keyword.prodname_imas_short}} Core + Maximo Manage by using its deployable architecture that is listed on {{site.data.keyword.cloud}} public catalog.

   The deployable architecture includes support for a {{site.data.keyword.redhat_openshift_full}} Kubernetes Service cluster with VPC Gen2 infrastructure.
