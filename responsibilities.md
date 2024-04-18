---

copyright:
  years: 2024
lastupdated: "2024-04-17"

subcollection: maximo-application-suite

keywords:

---

{{site.data.keyword.attribute-definition-list}}

# Understanding your responsibilities when you use _deployable-architecture-name_
{: #your-id}

<!-- The title of your H1 should be Understanding your responsibilities when you use _deployable-architecture-name_, where _deployable-architecture-name_ is the non-trademarked short version name of your deployable architecture. -->

Learn about the management responsibilities and terms and conditions that you have when you use the _deployable-architecture-name_ deployable architecture.
{: shortdesc}

- For more information about the responsibilities for you and for {{site.data.keyword.IBM}} when you use a deployable architecture, see [Understanding your responsibilities when you use deployable architectures](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures).
- For a high-level view of the service types in {{site.data.keyword.cloud}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for using {{site.data.keyword.cloud}} products](/docs/overview?topic=overview-shared-responsibilities).
- For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).

<!-- If you have additional responsibilities for you deployable architecture beyond what is covered in the overall "Understanding your responsibilities when you use deployable architectures" topic, include the next paragraph and group your items in the provided sections. If you don't, delete from here down. -->

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use the _deployable-architecture-name_ deployable architecture.

<!-- If you plan to list resource responsibility (see resources listed in each table in the platform shared responsibilities topic linked earlier) instead of individual tasks, you do not need to include rows for Hypervisor, Physical Servers and memory, Physical storage, Physical network and devices, and Facilities and data centers unless you need to indicate a 'Shared' or 'Customer' responsibility for one of the areas within those resources. -->

<!-- In the following sections, add tasks that are specific to your deployable architecture. Do not add tasks that are covered in the "Understanding your responsibilities when you use deployable architectures" that you link to earlier -->

## Incident and operations management
{: #incident-and-ops}

<!-- Use this section description exactly as worded. -->
<!-- When you have a topic that describes how a customer completes a task, link to it from the Your responsibilities column. -->

Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery.

|  | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Task 1| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 2| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 3| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
{: row-headers}
{: caption="Table 1. Responsibilities for incident and operations" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsibility for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}


## Change management
{: #change-management}

<!-- Use this section description exactly as worded. -->
<!-- When you have a topic that describes how a customer completes a task, link to it from the Your responsibilities column. -->

<!--
Review the first row of the change management table here. If your deployable architecture has compute resources that are not updated by your deployable architecture, include the row and list the resources that customers must update. (Red Hat OpenShift and Kubernetes are shown here as examples.)

If your deployable architecture does not have compute resources that customers must update, delete the row.
-->

Change management includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion.

|  | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
| Keep deployed services and resources up to date | N/A | Apply fixes and updates to the compute resources that are created from the deployable architecture. The following resources are not updated through the deployable architecture unless otherwise indicated.   \n * [Red Hat OpenShift clusters](/docs/openshift?topic=openshift-update)  \n * [Kubernetes lusters, worker nodes, and cluster components](/docs/containers?topic=containers-update) |
|Task 1| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 2| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
|Task 3| {{site.data.keyword.IBM_notm}} responsibility description  | Customer responsibility description |
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
