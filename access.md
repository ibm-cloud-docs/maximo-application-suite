---

copyright:
  years: 2024
lastupdated: "2024-04-24"

keywords: accessing, maximo application suite, deployable architecture, suite administrator

subcollection: maximo-application-suite

---


{{site.data.keyword.attribute-definition-list}}

# Accessing {{site.data.keyword.prodname_imas_short}}
{: #accessing}

After you install {{site.data.keyword.prodname_imas_full}} Core or {{site.data.keyword.prodname_imas_short}} Core + Maximo Manage, you can find the admin_url ({{site.data.keyword.prodname_imas_short}} administrator URL) to it under the
**Outputs** section on the project configuration page.
To find the login credentials for this URL, follow these steps:
1. Connect to the {{site.data.keyword.redhat_openshift_full}} cluster.
1. Select **Workloads > Secrets** from the navigation page.
1. Select the `mas-<mas_instance_id>-core` project.
1. Click the `<mas_instance_id>-credentials-superuser` secret.
1. Click the **Reveal values** link to get the username and password for {{site.data.keyword.prodname_imas_short}}.
1. Click the `<mas_instance_id>-cert-public` secret from the `mas-<mas_instance_id>-core` project.
1. Click the **Reveal values** link to get the contents of the certificates.
1. Retrieve the contents of > ca.crt file, which is the public certificate for {{site.data.keyword.prodname_imas_short}}.
1. After you import the public certificate into your browser's trusted store, paste the {{site.data.keyword.prodname_imas_short}} administrator URL into your browser and enter the authentication credentials to access the application.

You can now log in to {{site.data.keyword.prodname_imas_short}} to deploy applications, create users, and specify configuration.
