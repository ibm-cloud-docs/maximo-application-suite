---

copyright:
  years: 2024
lastupdated: "2024-04-17"

subcollection: maximo-application-suite

keywords:

---

{{site.data.keyword.attribute-definition-list}}

# Understanding your responsibilities when you use deployable architecture for {{site.data.keyword.prodname_imas_short}}
{: #deployable-architecure-responsibilities}


Learn about the management responsibilities and terms and conditions that you have when you use the {{site.data.keyword.prodname_imas_full}} deployable architecture.
{: shortdesc}

- For more information about the responsibilities for you and for {{site.data.keyword.IBM}} when you use a deployable architecture, see [Understanding your responsibilities when you use deployable architectures](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures).
- For a high-level view of the service types in {{site.data.keyword.cloud}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for using {{site.data.keyword.cloud}} products](/docs/overview?topic=overview-shared-responsibilities).
- For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use the {{site.data.keyword.prodname_imas_short}} deployable architecture.

<!-- If you plan to list resource responsibility (see resources listed in each table in the platform shared responsibilities topic linked earlier) instead of individual tasks, you do not need to include rows for Hypervisor, Physical Servers and memory, Physical storage, Physical network and devices, and Facilities and data centers unless you need to indicate a 'Shared' or 'Customer' responsibility for one of the areas within those resources. -->

<!-- In the following sections, add tasks that are specific to your deployable architecture. Do not add tasks that are covered in the "Understanding your responsibilities when you use deployable architectures" that you link to earlier -->

## Incident and operations management
{: #incident-and-ops}

Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery.

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Monitor the status of a deployable architecture| {{site.data.keyword.IBM_notm}} provides the ability for customers to monitor the lifecycle of the deployable architecture.  | Use the [needs attention widget](/docs/secure-enterprise?topic=secure-enterprise-needs-attention-projects) or [enable Event Notifications](/docs/secure-enterprise?topic=secure-enterprise-event-notifications-events&interface=ui) to monitor events that specifically impact the lifecycle of your deployable architecture. |
|Monitor the status of a product spun up by your deployable architecture| {{site.data.keyword.IBM_notm}} provides the ability for customers to monitor the lifecycle of the instances.  | Use the resource list, service instance pages, or the [Status](https://cloud.ibm.com/status){: external} page to monitor events that specifically impact your service instance. |
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
|Must use supported version of [{{site.data.keyword.cloud}} Terraform Provider](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures#change-management-da).| {{site.data.keyword.IBM_notm}} publishes Terraform provider of all Terraform enabled services on {{site.data.keyword.cloud}}.  | Customers should use the latest major version. Terraform Providers version requirements are documented within the `version.tf` file for each deployable architecture. |
|Third-party Terraform Providers used within templates| N/A  | Customer is responsible for any use of third-party Terraform code that is used with the deployable architecture. |
|Running default configuration (out of the box)| {{site.data.keyword.IBM_notm}} provides the ability for customers to create and deploy configurations of deployable architectures by using projects, Terraform-as-a-service, or the projects CLI.  | Use projects to [configure and deploy a deployable architecture](/docs/secure-enterprise?topic=secure-enterprise-config-project&interface=ui) |
|Running templates locally by using Terraform directly| N/A  | Customer can run the deployable architecture on their local system. |
|Customize modules or deployable architectures with pre-supported modules| {{site.data.keyword.IBM_notm}} provides and supports base Terraform modules for services on {{site.data.keyword.cloud}}, and provides preset JSON configuration overrides for templates.  | Customer can use these base Terraform modules to extend their base deployable architecture pattern. |
|Workload Management (Application Migration and Backup/Restore)| {{site.data.keyword.IBM_notm}} N/A  | Customer responsibility to manage and migrate application workloads. |
|Fixes, new features, and updates to the next major deployable architecture release| {{site.data.keyword.IBM_notm}} provides regular updates, bug fixes, and new features in a continuous delivery model that is apparent to the customer. IBM provides a migration path when possible.  | N/A |
|Keep deployed services and resources up to date| N/A | Apply fixes and updates to the compute resources that are created from the deployable architecture. These resources are not updated through the deployable architecture unless otherwise indicated. |
|Issues found in {{site.data.keyword.IBM_notm}}-provided versions of Terraform modules| {{site.data.keyword.IBM_notm}} provides a way for customers to open issues. If the issue is with a deployable architecture, open a case. If the issue is with a module, open an issue in the module [GitHub repo](https://github.com/terraform-ibm-modules){: external}.	 |
|Issues with {{site.data.keyword.IBM_notm}} container images| {{site.data.keyword.IBM_notm}} Issues with IBM container images.  | Customer provides information to reproduce any problem. |
|Issues with third party and open source container images| N/A  | Customer resolves with third-party vendor or open source community. |
|Issues with {{site.data.keyword.cloud_notm}}-provided stock operating system images| {{site.data.keyword.IBM_notm}} N/A  | Customer must get a compatible stock image from the vendor. |
|Issues with the services that the Terraform creates from a deployable architecture| {{site.data.keyword.cloud_notm}} resolves issues with the services.  | N/A |
|{{site.data.keyword.cloud_notm}} resource outages or issues that occur during automated template execution by using {{site.data.keyword.cloud_notm}} Terraform Provider| {{site.data.keyword.IBM_notm}} reports outages for any cloud resources on the [Status page](https://cloud.ibm.com/status){: external}.  | Customers can redeploy after issue is resolved. |
|{{site.data.keyword.cloud_notm}} catalog and private catalog support| {{site.data.keyword.IBM_notm}} provides a way for you to discover available deployable architectures in our public catalog and save your versions to a private catalog.  | N/A |
|Provide ability for drift detection| {{site.data.keyword.IBM_notm}} notifies you if your instantiated resources differ from the base pattern.  | Customer decides when to remediate any configurations detected in drift detection. |
| Pulling deployable architecture changes into a project| {{site.data.keyword.IBM_notm}} provides the ability for customers to update the version of a deployable architecture in a project if a new version becomes available. | Customers are notified when a [new deployable architecture version](/docs/secure-enterprise?topic=secure-enterprise-needs-attention-projects#na-version-update) is available so they can update their project. Customers can save their existing project data through an API, CLI, or by [exporting the project.json](/docs/secure-enterprise?topic=secure-enterprise-setup-project#json-export) from the UI. The saved information can be used as backup or as rollover plan if an issue exists. Customers can then test the deployable architecture changes by deploying in a development or test environment before they deploy to production.  These actions can all be completed within the same project. |
|Provide notice of end of support| {{site.data.keyword.IBM_notm}} provides notice through regular channels.  | N/A |
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
|Accessing deployed deployable architectures| {{site.data.keyword.IBM_notm}} provides the ability to control user access to resources provisioned through projects.  | Use Identity and Access Management (IAM) to [assign users access to projects](/docs/secure-enterprise?topic=secure-enterprise-access-project). |
|Authorize a project to deploy a deployable architecture configuration| {{site.data.keyword.IBM_notm}} provides the ability to authorize a project to deploy a deployable architecture configuration.  | Choose an authentication method to authorize a project to deploy in an account. It’s recommended to use a trusted profile, but you can use an API key or an existing secret to [authorize a project to deploy](/docs/secure-enterprise?topic=secure-enterprise-authorize-project) in an account. |
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
|Apply patches and security updates to operating system in customer instances| {{site.data.keyword.IBM_notm}} notifies you of updates.  | Customer must apply all updates. |
|Install software and OS patches into customer-managed virtual machines| N/A  | Customer must apply all patches. |
|Meet security and compliance objectives| Provide a secure deployable architecture that complies with declared standards. For more information about data security, see [How do I know that my data is safe?](/docs/overview?topic=overview-security)  | Secure your workloads and data. Integrate tools into your toolchains that satisfy your security and compliance requirements. To learn more about securing your cloud apps, see [Security to safeguard and monitor your cloud apps](https://www.ibm.com/cloud/architecture/architecture/practices/securing-cloud-native-apps-risks-mitigation/){: external}. |
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
|Meet disaster recovery objectives| {{site.data.keyword.IBM_notm}} follows best practices for disaster recovery. All {site.data.keyword.IBM} applications automatically recover and restart after any disaster event. For more information about disaster recovery, see the [{site.data.keyword.IBM_notm} Disaster Recovery Plan](/docs/overview?topic=overview-zero-downtime#disaster-recovery).  | Customers can help meet disaster recovery objectives by deploying their project in a development or test environment before they deploy to production. The customer does not have to take other actions to prepare for an event of a catastrophic failure in a region. |
|Meet high availability objectives| {{site.data.keyword.cloud}} is available globally and load balanced from a single URL. It is highly available and continues to run even if your resources are unavailable. For more information about high availability, see the [{site.data.keyword.IBM} service level objectives](/docs/overview?topic=overview-slo) and the [sample application architecture](/docs/overview?topic=overview-bcdr-app-recovery).  | N/A |
{: row-headers}
{: caption="Table 5. Responsibilities for disaster recovery" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsibility for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}
