---
title: Read audience
seo-title: Read audience
description: Read audience
seo-description: The Read audience activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.
uuid: 5d368b85-9743-46ca-b9fb-7a20d2829b37
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/read-audience
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 28.812-0400
cq-lastreplicated: 2018-07-23T05 57 05.960-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
cq-template: /apps/help/templates/article-3
discoiquuid: f5cee71e-4f0d-4e4f-864c-4e43be02e49a
firstPublishExternalDate: 2018-07-23T05:57:05.900-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 29.492-0400
jcr-createdby: admin
jcr-description: Read audience
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:05.900-0400
lochandoffdate: 2018-07-25T09 29 28.811-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Read audience
publishexternaldate: 2018-07-23T05 57 05.900-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/read-audience.html
sha1: 9a5fba2c56df841ad6239f584c6f3f73c56784a8
topicBrowsingSortDate: 2018-07-23T05:57:05.900-0400
index: y
internal: n
snippet: y
---

# Read audience

Read audience

## Description

![](assets/prefill.png)

The **Read audience** activity allows you to retrieve an existing audience and to refine it by applying additional filtering conditions.

## Context of use

The **Read audience** activity is a simpler version of the **Query** activity designed for cases where you only need to select an existing audience.

## Configuration

1. Drop a **Read audience** activity into your workflow.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the audience you want to retrieve from the **Properties** tab.

   You can retrieve audiences of the following types: **List**, **Query**, **File** and **Experience Cloud**. For more information on audience types, refer to the [Audiences](../../audiences/using/about-audiences.md) documentation.

   ![](assets/readaudience_activity1.png)

1. If you want to apply additional filtering to the selected audience, add conditions via the **Source filtering** tab of the activity.

   For more information about creating filtering conditions, refer to the [Creating queries](../../automating/using/editing-queries.md#creating-queries) documentation.

1. Confirm the configuration of your activity and save your workflow.

## Example: Reconcile a File audience with the database

This example shows how to use the **Read audience** activity to reconcile an audience directly created from a file import.

When performing a file import, you can directly save its content in an audience. This audience is a File audience and its data is not linked to any database resources.

The import workflow is designed as follows:

![](assets/readaudience_activity_example3.png)

* A [Load file](../../automating/using/load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

  For example:

  ```
  lastname;firstname;birthdate;email;crmID
  Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
  Mars;Daniel;17/11/1987;dannymars@example.com;123545
  Smith;Clara;08/02/1989;hayden.smith@example.com;124567
  Durance;Allison;15/12/1978;allison.durance@example.com;120987
  Lucassen;Jody;28/03/1988;jody.lucassen@example.com;127634
  Binder;Tom;19/01/1982;tombinder@example.com;128653
  Binder;Tommy;19/01/1915;tombinder@example.com;134576
  Connor;Jade;10/10/1979;connor.jade@example.com;132452
  Mack;Clarke;02/03/1985;clarke.mack@example.com;149876
  Ross;Timothy;04/07/1986;timross@example.com;157643
  ```

* A [Save audience](../../automating/using/save-audience.md) activity saves the incoming data as an audience. As the data has not been reconciled yet, the audience is a File audience and its data is not recognized as profile data yet.

The reconciliation workflow is designed as follows:

![](assets/readaudience_activity_example2.png)

* A **Read audience** activity uploads the File audience created in the import workflow. The audience data is not yet reconciled with the Adobe Campaign database.
* A [Reconciliation](../../automating/using/reconciliation.md) activity identifies the incoming data as profiles through its **Identification** tab. For example by using the **email** field as reconciliation criteria.
* An [Update data](../../automating/using/update-data.md) activity inserts and updates the profiles resource of the database with the incoming data. As the data is already identified as profiles, you can select the **Directly using the targeting dimension** option and select **Profiles** in the **Identification** tab of the activity. Then, you simply have to add the list of fields that need to be updated in the according tab.

## Example: Union on two refined audiences

The workflow defined in this example shows the union of two **Read audience** activities. The goal of this workflow is to send an email to Gold or Silver members that are between 18 and 30 years old.

Specific audiences are already created in the system to keep track of Gold and Silver members.

The workflow is designed as follows:

![](assets/readaudience_activity_example1.png)

* A first **Read audience** activity that retrieves the Gold members audience and refines it by selecting only profiles that are between 18 and 30 years old.
* A second **Read audience** activity that retrieves the Silver members audience and refines it by selecting only profiles that are between 18 and 30 years old.
* A **Union** activity that unites populations from both **Read audiences** activities into one final population.
* An **Email delivery** activity that sends the email to the population coming from the **Union** activity.
