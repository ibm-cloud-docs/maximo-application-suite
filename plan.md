---

copyright:
  years: 2024
lastupdated: "2024-05-09"

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

### Verify access role
{: #verifyrole}

IAM access roles are required to install this deployable architecture and create all the required elements.

You need the following permissions for this deployable architecture:
- Create services from {{site.data.keyword.cloud_notm}} catalog.
- Create and modify {{site.data.keyword.cloud_notm}} VPC services, virtual server instances, networks, network prefixes, storage volumes, SSH keys, and security groups of this VPC.
- Create and modify {{site.data.keyword.cloud_notm}} direct links and {{site.data.keyword.cloud_notm}} Transit Gateway.
- Access existing Object Storage services.

For information about configuring permissions, contact your {{site.data.keyword.cloud_notm}} account administrator.

### Access for {{site.data.keyword.cloud_notm}} projects
{: #access-ibmcloud-projects}

You can use {{site.data.keyword.cloud_notm}} projects as a deployment option. Projects are designed with infrastructure as code and compliance in mind to help ensure that your projects are managed, secure, and always compliant. For more information, see [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

You need the following access to create a project and create project tooling resources within the account. Make sure you have the following access:
- The Editor role on the Projects service.
- The Editor and Manager role on the Schematics service
- The Viewer role on the resource group for the project
    For more information, see [Assigning users access to projects](/docs/secure-enterprise?topic=secure-enterprise-access-project).

Before you install {{site.data.keyword.prodname_imas_short}} Core or {{site.data.keyword.prodname_imas_short}} Core + Manage, you must complete the following tasks.

1. Create an {{site.data.keyword.redhat_openshift_notm}} cluster
1. Obtain an {{site.data.keyword.IBM}} Entitled Registry key
1. Retrieve the {{site.data.keyword.cloud_notm}} API Key
1. Get the {{site.data.keyword.prodname_imas_short}} license file
1. Retireve the SLS license ID

Platform and Service {{site.data.keyword.cloud_notm}} IAM roles and policies are only used for the VPC, {{site.data.keyword.redhat_openshift_notm}}, and other {{site.data.keyword.cloud_notm}} resources, while the users and roles for {{site.data.keyword.prodname_imas_short}} are defined and managed within the product.
{: note}

### {{site.data.keyword.redhat_openshift_notm}} Cluster
{: #openshiftcluster}

You must have a target {{site.data.keyword.redhat_openshift_notm}} cluster ready to install {{site.data.keyword.prodname_imas_short}}.
If you do not already have one, then install it using {{site.data.keyword.redhat_openshift_notm}} Container Platform on VPC landing zone available on {{site.data.keyword.cloud_notm}} public catalog or refer to the {{site.data.keyword.redhat_openshift_notm}} Container Platform installation overview.
 - Make sure that your existing {{site.data.keyword.redhat_openshift_notm}} cluster has outbound access to `quay.io` registry site.
 - Make sure that the status of your {{site.data.keyword.redhat_openshift_notm}} cluster for the Master node is `Normal`, and that of Worker nodes, Add-ons, and Ingress is `Healthy`.

For more information about steps to deploy, see [Deploying {{site.data.keyword.redhat_openshift_notm}} Kubernetes Service VPC cluster](/docs/maximo-application-suite?topic=maximo-application-suite-deploy-redhat-openshift-kubernetes-service).

### Known limitations
{: #knownlimitations-rhocp}

- Compliance policies

    If you validate against FS Cloud compliance policy or stricter policies which require private network use, deploying {{site.data.keyword.prodname_imas_short}} on {{site.data.keyword.redhat_openshift_notm}} with VPC landing zone require changes (via override.json) to the default landing zone configuration that will:
    1. Open public gateway access to quay.io to pull {{site.data.keyword.prodname_imas_short}} operator images.
    1. Open public ingress through transit gateway to {{site.data.keyword.prodname_imas_short}} endpoints for console and api running on the workload cluster.

    These changes cause the FS Cloud profile rules that {{site.data.keyword.redhat_openshift_notm}} with VPC landing zone is validated against, to fail in Security and Compliance Center.

### {{site.data.keyword.IBM}} Entitled Registry key
{: #entitledregkey}

To access your software in the entitled registry, obtain an {{site.data.keyword.IBM}} Entitled Registry key.

For more information, see [Entitlement keys](https://myibm.ibm.com/products-services/containerlibrary){: external}.

### {{site.data.keyword.prodname_imas_short}} license
{: #maslic}

The {{site.data.keyword.prodname_imas_short}} license needs to be retrieved from the {{site.data.keyword.IBM}} License Key Center.

If you do not already have your {{site.data.keyword.prodname_imas_short}} license key file, you can create and download it in the {{site.data.keyword.cloud_notm}} License Key Center.

For more information, see [how to request specific license keys for IBM software products](https://www.ibm.com/support/pages/ibm-support-licensing-start-page){: external}.

### {{site.data.keyword.prodname_imas_short}} license ID
{: #maslicid}

A unique 12-character hexadecimal value in the first line of your {{site.data.keyword.prodname_imas_short}} license key file.
For example, `SERVER sls-rlks-0.rlks 0242ac110002 27000`, where the 12-character hexadecimal value is `0242ac110002`.

You can use a Secrets Manager to add the license key.

### {{site.data.keyword.cloud_notm}} API Key
{: #cloudapikey}

Your {{site.data.keyword.cloud_notm}} account's API key. The user who owns this key must be assigned the Administrator role.

If you do not have the API key, see
[Managing user API keys](/docs/account?topic=account-userapikey&interface=ui).
