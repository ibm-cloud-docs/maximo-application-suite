---

copyright:
  years: 2024
lastupdated: "2024-04-17"

subcollection: maximo-application-suite

keywords:

---

{{site.data.keyword.attribute-definition-list}}

# Understanding your responsibilities when you use deployable architecture for Maximo Application Suite
{: #deployable-architecure-responsibilities}


Learn about the management responsibilities and terms and conditions that you have when you use the IBM Maximo Application Suite deployable architecture.
{: shortdesc}

- For more information about the responsibilities for you and for {{site.data.keyword.IBM}} when you use a deployable architecture, see [Understanding your responsibilities when you use deployable architectures](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures).
- For a high-level view of the service types in {{site.data.keyword.cloud}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for using {{site.data.keyword.cloud}} products](/docs/overview?topic=overview-shared-responsibilities).
- For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use the Maximo Application Suite deployable architecture.

<!-- If you plan to list resource responsibility (see resources listed in each table in the platform shared responsibilities topic linked earlier) instead of individual tasks, you do not need to include rows for Hypervisor, Physical Servers and memory, Physical storage, Physical network and devices, and Facilities and data centers unless you need to indicate a 'Shared' or 'Customer' responsibility for one of the areas within those resources. -->

<!-- In the following sections, add tasks that are specific to your deployable architecture. Do not add tasks that are covered in the "Understanding your responsibilities when you use deployable architectures" that you link to earlier -->

## Incident and operations management
{: #incident-and-ops}

Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery.

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Monitor the status of a deployable architecture| {{site.data.keyword.IBM_notm}} provides the ability for customers to monitor the lifecycle of the deployable architecture.  | Use the [needs attention widget](docs/secure-enterprise?topic=secure-enterprise-needs-attention-projects) or [enable Event Notifications](docs/secure-enterprise?topic=secure-enterprise-event-notifications-events&interface=ui) to monitor events that specifically impact the lifecycle of your deployable architecture. |
|Monitor the status of a product spun up by your deployable architecture| {{site.data.keyword.IBM_notm}} provides the ability for customers to monitor the lifecycle of the instances.  | CUse the resource list, service instance pages, or the [Status](https://cloud.ibm.com/status){: external} page to monitor events that specifically impact your service instance. |
{: row-headers}
{: caption="Table 1. Responsibilities for incident and operations" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or {{site.data.keyword.IBM_notm}} might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}


## Change management
{: #change-management}

<!-- Use this section description exactly as worded. -->
<!-- When you have a topic that describes how a customer completes a task, link to it from the Your responsibilities column. -->

<!--
Review the first row of the change management table here. If your deployable architecture has compute resources that are not updated by your deployable architecture, include the row and list the resources that customers must update. (Red Hat OpenShift and Kubernetes are shown here as examples.)

If your deployable architecture does not have compute resources that customers must update, delete the row.
-->

Change management includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion.

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
| Keep deployed services and resources up to date | N/A | Apply fixes and updates to the compute resources that are created from the deployable architecture. The following resources are not updated through the deployable architecture unless otherwise indicated.   \n * [Red Hat OpenShift clusters](/docs/openshift?topic=openshift-update)  \n * [Kubernetes lusters, worker nodes, and cluster components](/docs/containers?topic=containers-update) |
|Creation of the {{site.data.keyword.cloud}} deployable architectures| {{site.data.keyword.IBM_notm}} provides the base pattern as a deployable architecture for instantiation through Terraform.  | N/A |
|Must use supported version of [{{site.data.keyword.cloud}} Terraform Provider](docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures#change-management-da).| {{site.data.keyword.IBM_notm}} publishes Terraform provider of all Terraform enabled services on {{site.data.keyword.cloud}}.  | Customers should use the latest major version. Terraform Providers version requirements are documented within the `version.tf` file for each deployable architecture. |
|Task 3| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 4| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 5| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 6| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 7| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 8| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 9| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 10| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 11| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 12| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 13| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 14| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 15| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 16| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 17| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 18| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 19| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
{: row-headers}
{: caption="Table 2. Responsibilities for change management" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsibility for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}


## Identity and access management
{: #iam-responsibilities}

<!-- Use this section description exactly as worded. -->
<!-- When you have a topic that describes how a customer completes a task, link to it from the Your responsibilities column. -->

Identity and access management includes tasks such as authentication, authorization, access control policies, and approving, granting, and revoking access.

|  | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Task 1| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 2| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 3| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
{: row-headers}
{: caption="Table 3. Responsibilities for identity and access management" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsibility for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Security and regulation compliance
{: #security-compliance}

<!-- Use this section description exactly as worded. -->
<!-- When you have a topic that describes how a customer completes a task, link to it from the Your responsibilities column. -->

Security and regulation compliance includes tasks such as security controls implementation and compliance certification.

|  | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Task 1| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 2| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 3| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
{: row-headers}
{: caption="Table 4. Responsibilities for security and regulation compliance" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsibility for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Disaster recovery
{: #disaster-recovery}

<!-- Use this section description exactly as worded. -->
<!-- When you have a topic that describes how a customer completes a task, link to it from the Your responsibilities column. -->

Disaster recovery includes tasks such as providing dependencies on disaster recovery sites, provision disaster recovery environments, data and configuration backup, replicating data and configuration to the disaster recovery environment, and failover on disaster events.

|  | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Task 1| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 2| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 3| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
{: row-headers}
{: caption="Table 5. Responsibilities for disaster recovery" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsibility for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}
