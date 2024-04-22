---

copyright:
  years: 2024
lastupdated: "2024-04-22"

keywords: accessing, maximo application suite, deployable architecture, suite administrator

subcollection: maximo-application-suite

---


{{site.data.keyword.attribute-definition-list}}

# Accessing {{site.data.keyword.prodname_imas_short}}
{: #accessing}

After you install {{site.data.keyword.prodname_imas_full}}, you need the following items of information to access it:

- The {{site.data.keyword.prodname_imas_short}} administrator URL, which you use to connect to {{site.data.keyword.prodname_imas_short}} through a browser.
- Your username and password.
- The public certificate for {{site.data.keyword.prodname_imas_short}}. You import this certificate into your browser's trusted store to make sure that a secure communication between your browser and {{site.data.keyword.prodname_imas_short}} is established.

How you retrieve these items of information depends on whether you opted for the email notification during the deployment.

If you provide the correct SMTP configuration during the deployment, you can retrieve the administrator URL, username, and password from the emails that you received. The public certificate is attached to these emails.

If you do not opt for the email notification, you can retrieve the administrator URL and credentials of the {{site.data.keyword.redhat_openshift_full}} cluster from the deployment that is created in the boot node’s resource group. However, to retrieve your username, password, and the public certificate of {{site.data.keyword.prodname_imas_short}}, you must connect to the {{site.data.keyword.redhat_openshift_notm}} cluster.

For more information, see [Accessing {{site.data.keyword.prodname_imas_short}}](https://www.ibm.com/docs/en/mas-cd/continuous-delivery?topic=installing-accessing-maximo-application-suite){: external}.
