---
title: Release Notes 2015-2016
description: This page lists all 2015 and 2016 releases of Adobe Campaign Standard.
page-status-flag: never-activated
uuid: d5a0f6cc-0bed-46cf-8dff-1717fb624f8f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: a3ce6b80-1858-49d1-8880-3543181127f4

internal: n
snippet: y
---

# Release Notes 2015-2016{#release-notes}

Looking for a specific 2015-2016 release of Adobe Campaign Standard?

Each release comes with new features and patches. Click on a release to view its content.

View the latest [documentation updates](../../rn/using/documentation-updates.md) for Adobe Campaign Standard. If you're looking for a newer release, consult this [page](../../rn/using/release-notes.md).

## Release 16.11 - November 2016 {#release-16-11---november-2016}

### New capabilities {#new-capabilities}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Deliverability exclusion rules<br /> </td> 
   <td> An encrypted global suppression list is now managed in the deliverability instance to avoid being blacklisted due to malicious activity, especially the use of a Spamtrap.<br /> For each email delivery, two default typology rules compare the recipient email addresses with the forbidden addresses or domain names contained in this list. If there is a match, that recipient is excluded from the target population.<br /> For more information, refer to the <a href="../../administration/using/filtering-rules.md#default-deliverability-exclusion-rules">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> General optimization<br /> </td> 
   <td> This update includes numerous changes and patches that fix issues encountered by our clients. The global platform performances have also been optimized. <br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches}

#### General {#general}

* Fixed several security issues.
* Fixed several issues regarding empty fields or duplicate fields in the REST API.
* You can now create SMS messages and push notifications directly from the home page of the application.

#### Emails and SMS messages {#emails-and-sms-messages}

* Fixed an issue that prevented users from uploading zip files in the content editor.
* Fixed an issue that prevented opening a proof after sending it.
* Fixed an issue that led to an error message displaying when accessing the **[!UICONTROL Hot Clicks]** report on an A/B test email.
* Fixed an issue that prevented modifications made using the **[!UICONTROL Show source]** mode from being applied.
* Fixed an issue that could prevent predictive subject line xml model files from being imported.
* A new screen dedicated to importing data for the subject line trained model is now available in **[!UICONTROL Administration > Channels > Emails > Predictive Subject Line]** .
* Fixed an issue that allowed non admin users to edit the authorized masks in the email configuration screen.

#### Push notifications {#push-notifications}

* Fixed an issue that prevented sending logs and event logs from being displayed for the recipients after sending a push notification using the **[!UICONTROL Send push on profiles]** template.
* Fixed an issue that could prevent new mobile applications from being created.

#### Workflows {#workflows}

* Fixed a performance issue that occured when using the **[!UICONTROL Subscription]** activity.
* Fixed an issue that prevented a workflow from functioning when its internal name contained a space.

#### Integrations {#integrations}

* Fixed an issue that could lead to an error being displayed when using the **Image shared from Adobe Marketing Cloud** option in an email.

#### Custom resources {#custom-resources}

* Enhanced APIs log preview between two publications of extended API fields.
* Fixed an issue that prevented a custom resource from being deleted before it was published.
* Fixed an issue that prevented profiles from being extended and identifier keys from being set with a dynamic field.
* Fixed an issue that could occur when adding links in a custom resource.

## Release 16.10 - October 2016 {#release-16-10---october-2016}

### New capabilities {#new-capabilities-1}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Email predictive subject line<br /> </td> 
   <td> When editing an email, a new option lets you try out different subject lines and get an estimation of its open rate before you send it. This is made possible by training your own model based on your past delivery data or by using a pre-defined model that is specific to your industry. This feature is available for email messages and for databases that contain English contents only. <br /> For more information about enabling and using it, refer to the <a href="../../designing/using/subject-line.md#predictive-subject-line">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> SMS transactional messaging<br /> </td> 
   <td> The SMS channel has been added to Adobe Campaign's transactional messaging capabilities. Two channels are now supported for transactional messages: email and SMS.<br /> For more information, refer to the <a href="../../administration/using/configuring-transactional-messaging.md#creating-an-event">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Follow-up message for transactional messaging<br /> </td> 
   <td> It is now possible to create a workflow targeting an event. This means that you can send a follow-up message to the customers who previously received a transactional message. You can filter the target by the event type, the event broadlogs and the tracking logs. In the follow-up message, you will be able to leverage the content of the event (payload). <br /> For more information, refer to the <a href="../../channels/using/follow-up-messages.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Extended Profile &amp; Services API<br /> </td> 
   <td> You can now expose extended fields in the Profile and Services API. The publication mechanism allows APIs to map the extended fields of the Profiles or Services custom resources. For this to work, the <strong>Datamodel</strong> role has been added. This new role allows the user to configure a set of administrators who will have access to the data model.<br /> For more information, refer to the <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-1}

#### General {#general-1}

* Fixed several security issues.

#### Emails and SMS messages {#emails-and-sms-messages-1}

* The SMS external account configuration screen ( **[!UICONTROL Administration > Channels > SMS > SMS accounts]** ) has been improved. Several parameters have been added in the **[!UICONTROL SMSC specifics]** section to support error codes in the "Text" field.

#### Push notifications {#push-notifications-1}

* Fixed an issue that prevented the predefined filters from being displayed when editing the audience of a push notification based on the **[!UICONTROL Send via push notification]** (mobileApp) template.
* The mobile application configuration screen ( **[!UICONTROL Administration > Channels > Push Notification > Mobile applications]** ) now displays a message to indicate that the iOS or Android platform has been successfully created.

#### Landing pages {#landing-pages}

* Fixed issues that prevented confirmation emails from being sent when a landing page form was submitted.

#### Audiences and queries {#audiences-and-queries}

* Fixed several issues that occurred when selecting a profile in the query editor.

#### Transactional messages {#transactional-messages}

* Fixed an error that prevented a transactional template from being unpublished.
* Fixed an issue that led to trigger events being displayed in the event list.

#### Integrations {#integrations-1}

* Fixed an issue that prevented a shared audience from being used in a delivery after that audience was updated.
* Fixed an issue that prevented a shared asset ( **[!UICONTROL Image shared from Adobe Marketing Cloud]** option) from being used in a landing page.
* Fixed issues that occurred when editing a shared audience imported from Adobe Audience Manager.

## Release 16.9 - September 2016 {#release-16-9---september-2016}

### New capabilities {#new-capabilities-2}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Remarketing Triggers<br /> </td> 
   <td> Integration between the core service <span class="uicontrol">Triggers</span> and Adobe Campaign allows you to send personalized emails to your customers as a reaction to specific behaviors that are tracked on your website by Adobe Analytics (within 15 minutes).<br /> In Adobe Marketing Cloud, you define the different triggers, that is to say, the customer behaviors that you would like to monitor, such as all of the clients who abandoned their cart or their form, removed a product from their cart, or even the clients whose session expired. When creating a trigger, you define the trigger's condition and the data that will be sent in the event (pload) to Adobe Campaign. <br /> In Adobe Campaign, you select the trigger that was previously created, you enrich the event data with datamart data and you define a transactional message template linked to that trigger. For example, when a client abandons their cart, an event is sent to Adobe Campaign which can then leverage this event via a remarketing email that is sent to the client within 15 minutes.<br /> For more information, refer to the <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional messages: Pause / Unpublish<br /> </td> 
   <td> You can now suspend the publication of a transactional template while you update its content. The corresponding messages are no longer sent, but they are stored in the database. When resuming, the queued messages are processed and they are sent if they have not expired.<br /> For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication">detailed documentation</a>.<br /> You can now also unpublish events and transactional templates. The corresponding messages are not sent anymore and they are not stored in the database.<br /> For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Multibranding<br /> </td> 
   <td> Clients with multiple brands can now manage them in the same instance. Branding is a feature managed by the administrator of your Adobe Campaign instance that allows you to centrally configure all of the parameters related to a brand within Adobe Campaign. This includes things such as the logo to more technical parameters like tracking URLs, Web Analytics, server URL, domain name, etc.<br /> For more information, refer to the <a href="../../administration/using/branding.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Responsive email design preview<br /> </td> 
   <td> This feature allows you to test your email's responsiveness on different types of devices. In the email preview, a grid has been added to test your email on various screen sizes.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push notifications<br /> </td> 
   <td> A new channel has been added to allow marketers to send personalized and segmented push notifications on iOS and Android mobile devices. Messages can be sent through a single delivery or using a workflow activity. Compatibility with Transactional messaging will be available in future versions. This channel leverages the Mobile core service’s SDK (available <a href="https://marketing.adobe.com/developer/gallery/marketing-cloud-mobile-libraries">here</a>).<br /> For more information, refer to the <a href="../../channels/using/about-push-notifications.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-2}

#### General {#general-2}

* This release introduces new filtering and searching capabilities in the interface lists. This new feature is available, for example, in the logs (delivery, tracking), services (subscription, subscription history), audiences and workflow transitions.
* Fixed several display issues regarding the number of touchpoints in a customer profile.
* Fixed several typology issues.

#### Emails and SMS messages {#emails-and-sms-messages-2}

* Fixed an error that allowed erroneous proofs to be edited. They are now read-only. 
* Fixed an issue that led a recipient being blacklisted when an SMS was too long or had encoding problems.

#### Custom resources {#custom-resources-1}

* Fixed an error that prevented all of the results from being displayed when using a custom resource's advanced filters.

#### Transactional messages {#transactional-messages-1}

* A prefix is now automatically added to the identifier of a new event definition.
* The icon representing the transactional messages in the interface has been changed.

#### Integrations {#integrations-2}

* Fixed a display error that would occur when a high resolution image was inserted via the **Dynamic image from Adobe Target** option.
* Fixed an error that allowed a shared audience to be saved even if the destination ID was not set in AMC Data Source.

## Release 16.7 - July 2016 {#release-16-7---july-2016}

### New capabilities {#new-capabilities-3}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Enriched transactional messages<br /> </td> 
   <td> You can now link transactional templates with the Adobe Campaign database to recover information that allows you to enrich the content of your transactional messages.<br /> For more information, refer to the <a href="../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic URLs for images<br /> </td> 
   <td> This new functionality allows you to personalize an image source by inserting content blocks and dynamic text for tracking and personalization purposes.<br /> It then becomes possible, amongst other things, to profit from the functionalities of AEM Asset (S7) dynamic media by entering parameters into the image URLs. For example, you can send an email with personalized images stating "Hello Alexandre, get the latest news about upcoming events in Paris!" or "Hello Frank, get the latest news about upcoming events in New York!".<br /> For more information, refer to the <a href="../../designing/using/personalization.md#personalizing-urls">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration with People Core Service<br /> </td> 
   <td> The Adobe Marketing Cloud <strong>Declared IDs</strong> are now covered by the integration between Adobe Campaign and People Core Service (Profiles &amp; Audiences).<br /> This means that you can import segments and export audiences made up of <strong>Visitor ID</strong>s or <strong>Declared ID</strong>s.<br /> For more information, refer to the <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery logs<br /> </td> 
   <td> The MTA logs (delivery server) now display the complete history of each message, particularly all of the delivery attempts as well as the associated error statuses, and this has no impact on the application's performance.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-3}

#### General {#general-3}

* Fixed an error that could cause irrelevant fields to be displayed instead of fields that need to be completed. This would happen after the comparison operator was modified multiple times when editing a condition in a query.
* Fixed the behavior of the option **[!UICONTROL The last X days/months/quarters/years]** when defining a relative filtering condition for a date field. The period calculated is now a sliding period relative to the date and time of the server and not calendar-based.

#### Workflows {#workflows-1}

* Fixed an error that would return an incorrect list of values in the screen for selecting the targeting dimension in the properties of a **[!UICONTROL Query]** activity.
* Fixed an error that would force the **Exists** operator to be selected when adding an average or count aggregate on a collection element in a **[!UICONTROL Query]** activity.

#### Content editing {#content-editing}

* Fixed an error that could lead to display problems (responsive design) when importing HTML content: the style attributes are no longer rewritten when the content is opened for the first time after being imported.
* Fixed a non-blocking error that was caused when a condition was added on a dynamic content variant.
* Fixed an error caused by adding a checkbox in the content of a landing page. The checkbox was unusable.
* Fixed an error that could occur when deleting text in a block if the cursor was placed at the start of the block in question.

#### Transactional messages {#transactional-messages-2}

* When integrating a website, you can now define an expiration date for any given event. Once this date has been passed, the message corresponding to the event can no longer be sent.

## Release 16.6 - June 2016 {#release-16-6---june-2016}

### New capabilities {#new-capabilities-4}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Profiles and Services API<br /> </td> 
   <td> The Adobe Campaign <span class="uicontrol">Profiles and Services</span> API is available in the <a href="https://www.adobe.io/products/campaign">adobe.io</a> portal. This allows Adobe Campaign profiles to be updated, added, and deleted, and for them to be subscribed to or unsubscribed from services via REST calls.<br /> For more information, refer to the <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">detailed description of the API</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-4}

#### General {#general-4}

* Tooltips are now disabled on mobile devices to ensure that the information displayed on the screen is easy to read.
* Fixed an error that prevented the user from scrolling the content of certain zones on the iPad screen.
* Fixed several compatibility errors encountered while editing content in Internet Explorer 11.
* Fixed an error that could prevent detailed logs from being accessed when the data import failed for the first time.
* Fixed an error that could prevent a range filter from being saved.
* Fixed an error that prevented elements of a resource from being displayed when configuring the way a list is displayed.
* Fixed an error in the query editor explorer. The results returned by the search field were kept in the search history and continued to be displayed upon every new search.

#### Emails and SMS messages {#emails-and-sms-messages-3}

* Fixed an error that prevented information linked to bounces from being recovered in delivery logs.
* Fixed an error that prevented the context in a dynamic content block of a transactional message from being accessed.
* Fixed an error that prevented a URL link from being defined on dynamic text in an email's content.
* Fixed the display of the top bar of the delivery creation wizard.
* The primary key of a delivery can no longer be used as a personalization field.

#### Workflows {#workflows-2}

* The transitions between two activities of a workflow now display the count of elements computed and transferred from one activity to another.
* Incompatible fields are now hidden when additional data is added in a **[!UICONTROL Query]** activity.
* The aggregate definition window, displayed when adding additional data, was improved to only offer options that are compatible with the data in use (for example: calculating an average is only possible for numerical data).
* Starting or restarting an out-of-the-box technical workflow can now only be carried out by a user with administration rights.

#### Landing pages {#landing-pages-1}

* Fixed an error that could truncate 32 bit AES coding keys in the properties of a landing page.
* Fixed an error that prevented the query editor from displaying correctly when defining a visibility condition or when adding dynamic content to a landing page.

#### Custom resources {#custom-resources-2}

* The **[!UICONTROL Switch to parameters]** option is now hidden when defining a filter related to a profile's subscriptions to a service.
* Fixed an error that could occur when a 0-1 type link was configured from a custom resource.
* Fixed an error that, where relevant, could prevent the defined **Constant default value** from being edited when adding a **Date and time** type field in a custom resource.

## Release 16.5 - May 2016 {#release-16-5---may-2016}

### New capabilities {#new-capabilities-5}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Predefined filters<br /> </td> 
   <td> Administrators can now create advanced filters that appear in the query editor in the form of pre-configured rules. Selecting those filters allows users to develop complex configurations more easily in a simplified interface when defining an audience, for example.<br /> For more information, refer to the <a href="../../developing/using/configuring-filter-definition.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Subscription Services<br /> </td> 
   <td> A new <span class="uicontrol">Subscription Services</span> activity offers the possibility of subscribing several profiles to a service or unsubscribing them from a service with in a single action.<br /> This activity can be used after having carried out a targeting or imported a file with identified data.<br /> For more information, refer to the <a href="../../automating/using/subscription-services.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: data enrichment<br /> </td> 
   <td> The <span class="uicontrol">Additional data</span> tab is now available in <span class="uicontrol">Query</span> type activities. This functionality lets you enrich the data targeted by the query and transfer this data to the following workflow activities where it can be exploited.<br /> After having added additional data, you can apply an additional filter level to the initially targeted data by creating conditions based on the defined additional data.<br /> For more information, refer to the <a href="../../automating/using/query.md#enriching-data">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Contextual help<br /> </td> 
   <td> A contextual help function is now available across the different Adobe Campaign screens. This means that, in a single click, you can directly access the documentation on the functionality that you are currently using. To display contextual help, click the '?' icon in the upper-right corner of the screen, as shown in the example below.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-5}

#### General {#general-5}

* Various interface New capabilities complying with Marketing Cloud standards.
* Standardization of the different drop-down list types.

#### Emails and SMS messages {#emails-and-sms-messages-4}

* Fixed an error that prevented emails from being sent if the error address mask was specified.
* The TLS protocol is now supported for email delivery. A new column in MX management lets you define the desired TLS behavior for each domain.
* The SMS interface has been improved.

#### Workflows {#workflows-3}

* Various workflow interface New capabilities.
* Fixed an error that occurred when displaying Quick actions.
* Fixed an error that could cause a workflow to fail when using a **[!UICONTROL Segmentation]** type activity containing a 1-N link.
* Fixed an error that prevented the transitions of a workflow from being opened on a hybrid device. 
* Fixed an error that prevented the pause button from being displayed when starting a workflow for the first time.

#### Content editor {#content-editor}

* The content editor now allows you to personalize any URL contained in an email or a landing page. Refer to the [detailed documentation](../../designing/using/personalization.md#personalizing-urls).
* Fixed an error that could cause images to be lost when they were added in the delivery's creation wizard and their content was modified afterwards.

#### Custom resources {#custom-resources-3}

* Fixed an error that occurred when adding a personalized 1-N type link in the configuration screen of a custom resource.
* Improved the display of the progress bar when preparing and publishing custom resources.
* Fixed an error that occurred when displaying a custom resource's list of links.

#### Transactional messages {#transactional-messages-3}

* The user-friendliness of the interface as well as the performance and robustness of the transactional message engine have been optimized.
* It is now possible to temporarily suspend the publication of a transactional message template. For more on this, refer to the [detailed documentation](../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication).
* Fixed an error that could cause a content block with an incompatible targeting dimension to be added into a transactional message template.
* Fixed an error that prevented the API preview from being displayed in an event configuration screen.

#### Audiences and queries {#audiences-and-queries-1}

* Various patches regarding the use of dates in the query editor. Refer to the [detailed documentation](../../automating/using/editing-queries.md#creating-queries).

#### Administration {#administration}

* Fixed an error regarding the name of the "Standard users" security group, that prevented users from logging in.

## Release 16.3 - March 2016 {#release-16-3---march-2016}

### New capabilities {#new-capabilities-6}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Interface and navigation<br /> </td> 
   <td> The Adobe Campaign interface was improved to make navigation and operations simple and intuitive.<br /> You now navigate from the top bar of the application. The advanced menus are accessible by selecting the <strong>Adobe Campaign</strong> logo.<br /> For more information, refer to the <a href="../../start/using/interface-description.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Save audience<br /> </td> 
   <td> A new option, <span class="uicontrol">Create then update an audience</span> , is now available in the <span class="uicontrol">Save audience</span> activity. This option allows you to manually enter an audience label. If the label entered corresponds to an existing audience, it will be updated. If the audience does not exist, it will be created.<br /> In addition, the audience will be updated every time the workflow is executed (again).<br /> You can always select the audience update mode: complete the audience with new data or replace the whole of the audience data at every execution.<br /> For more information, refer to the <a href="../../automating/using/save-audience.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Segmentation<br /> </td> 
   <td> The <span class="uicontrol">Segmentation</span> activity now allows the user to segment the data of a temporary resource. For example: the data of an imported file.<br /> For more information, refer to the <a href="../../automating/using/segmentation.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-6}

#### General {#general-6}

* Fixed a display error that occurred when sorting a list: the arrow indicating the sort order of a column could only be inversed for certain types of data.
* Fixed an error that limited the number of elements displayed in a drop-down menu when a rule was added in a query.

#### Emails and SMS messages {#emails-and-sms-messages-5}

* Fixed an error that could prevent access to the email rendering report.
* The prepare send stage for a message now returns an error if the sender address is not provided.

#### Workflows {#workflows-4}

* Certain file formatting options were visible but not taken into account when a CSV format file was extracted. These options are now no longer visible.
* Fixed an error caused when the **[!UICONTROL Delete the source files after transfer]** option was checked for a **[!UICONTROL SFTP]** type file transfer.
* Fixed an error that could prevent the counter and preview of **[!UICONTROL Query]** data from being displayed after refreshing the page.
* Fixed an error caused by opening certain transitions in a workflow, particularly after a delivery activity or a query in which the targeting and filtering dimensions were different.
* Fixed an error that prevented a personalization field from being inserted into a delivery activity of a workflow if the workflow was not saved after adding the activity.
* Fixed an error that prevented the outbound transition targeting dimension of an email delivery activity from being displayed.

#### Landing pages {#landing-pages-2}

* Fixed an error that prevented the personalization fields from functioning correctly in a localizable content block in a landing page.

#### Custom resources {#custom-resources-4}

* Fixed an error that prevented a search on a custom resource from being carried out if the **[!UICONTROL Add search fields]** option of the resource screen definition was checked and if several fields were selected in the **[!UICONTROL Filter zone composition]** .

## Release 16.2 - February 2016 {#release-16-2---february-2016}

### New capabilities {#new-capabilities-7}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> A/B test for emails<br /> </td> 
   <td> You can now carry out A/B tests on the content, subject, or sender name of your emails. This new functionality can test up to three variants of an element.<br /> When creating an email from one of the new templates specific to A/B tests, a new step in the creation wizard allows you to define the parameters of your test.<br /> For more information, refer to the <a href="../../channels/using/designing-an-a-b-test-email.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Brand management<br /> </td> 
   <td> You can now define one or several brands to centrally enter the parameters that affect a brand's identity. Adobe Campaign allows you to create these brands and link them to delivery or landing page templates.<br /> For more information, refer to the <a href="../../administration/using/branding.md#assigning-a-brand-to-an-email">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Incremental query<br /> </td> 
   <td> A new workflow activity, <span class="uicontrol">Incremental query</span> , allows you to carry out a query which, on every execution, targets only the new results. The results of previous executions are automatically excluded. Linked to a <span class="uicontrol">Scheduler</span> activity, you can define the execution frequency of the <span class="uicontrol">Incremental query</span> .<br /> For more information, refer to the <a href="../../automating/using/incremental-query.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional messages<br /> </td> 
   <td> The user friendliness of the transactional messages interface has been improved. All business process management linked to transactional messages is currently centralized in the <span class="uicontrol">Marketing plans</span> &gt; <span class="uicontrol">Transactional messages</span> menu. Event configuration has also been improved. Events are now managed independently from custom resources.<br /> For more information, refer to the <a href="../../channels/using/about-transactional-messaging.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-7}

#### General {#general-7}

* Fixed several display errors in reports, lists, and queries.
* Fixed several compatibility and display errors on mobile devices.

#### Emails and SMS messages {#emails-and-sms-messages-6}

* Fixed an error that could prevent the button used to insert personalization fields from displaying when creating a message (email or SMS).
* Fixed an error that could prevent SMS messages sent via Mblox from being correctly transmitted.

#### Audiences and queries {#audiences-and-queries-2}

* Fixed a counting error that could be caused when adding an additional condition in a query, after having modified the filtering dimension.
* Fixed an error that could lead to an incorrect pagination when previewing results of a query.

#### Content editing {#content-editing-1}

* Fixed an error that could prevent the dynamic content configuration from being correctly taken into account when using a personalized enumeration.

#### Workflows {#workflows-5}

* Fixed an error that could prevent any action in a workflow from being carried out if there was an empty line in the **[!UICONTROL Fields to update]** tab of an **[!UICONTROL Update data]** activity.
* Fixed an error that prevented data containing geographical/organizational unit information from being imported.
* Fixed an error caused by adding a **[!UICONTROL Change axis]** type of **[!UICONTROL Exclusion]** rule.
* Fixed an error that could lead to an unwanted additional segment being created when manipulating an outbound transition of a **[!UICONTROL Segmentation]** activity.
* Fixed an error caused by loading a file in a workflow template.
* Fixed an error that could prevent spaces from being used as column separators in a **[!UICONTROL Load file]** activity.

#### Custom resources {#custom-resources-5}

* Fixed an error that prevented the status of a custom resource from being re-drafted after importing a package, if the resource was published at the time of the export.

#### Packages {#packages}

* Fixed an error that prevented a package containing a workflow from being exported.
* Fixed an error that could prevent several elements of the same resource from being selected.

## Release 16.1 - January 2016 {#release-16-1---january-2016}

### New capabilities {#new-capabilities-8}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Reports<br /> </td> 
   <td> The following email specific reports have been added: <span class="uicontrol">Complaints</span> , <span class="uicontrol">Opens</span> , and <span class="uicontrol">Unsubscriptions</span> .<br /> The following reports have been improved: <span class="uicontrol">Delivery summary</span> , <span class="uicontrol">Bounce summary</span> , <span class="uicontrol">Delivery throughput</span> , and <span class="uicontrol">Tracking indicators</span> .<br /> For more information, refer to the <a href="../../reporting/using/defining-the-report-period.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Query editing<br /> </td> 
   <td> The query editor has been improved and now allows you to scan the <strong>1-N</strong> type links.<br /> For more information, refer to the <a href="../../automating/using/editing-queries.md#creating-queries">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content personalization<br /> </td> 
   <td> As for email or landing page editing, the input interface for content block display conditions has been improved.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: column definition when importing<br /> </td> 
   <td> The <span class="uicontrol">Load file</span> activity now allows you to configure the columns of an imported file in detail: expected data type, date and time format, processing to apply in case of an empty value or an error, and value remapping.<br /> For more information, refer to the <a href="../../automating/using/load-file.md#column-format">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mapping of SMS encodings<br /> </td> 
   <td> It is now possible to define mappings of encodings of personalized SMS messages for providers not using standard encoding. An administrator can carry out the configuration of personalized mappings and define the order in which they are supposed to be taken into account.<br /> For more information, refer to the <a href="../../administration/using/configuring-sms-channel.md#smsc-specifics">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-8}

#### General {#general-8}

* Improved compatibility with Internet Explorer and Chrome for hybrid/touchscreen devices.
* Fixed an error that could lead to the loss of all data entered for a new user/profile/test profile if the indicated email address contained syntax errors.

#### Emails and SMS messages {#emails-and-sms-messages-7}

* Fixed an error that could prevent the content thumbnail from being generated in the email preview screen.
* Fixed an error that could prevent the raw content of a message (email or SMS) from being displayed in the message preview screen.

#### Audiences and queries {#audiences-and-queries-3}

* Fixed an error that could prevent a **Query** type audience from being created in the **Service** resource.
* Fixed an error that could prevent the function list from being displayed correctly when editing a condition of a query in advanced mode.
* Fixed an error that could prevent a **Query** type audience from being created if it contained criteria based on collections.
* Fixed an error that could prevent queries containing filters on delivery KPIs from being created.
* Fixed an error that could prevent the content of an audience created from a workflow from being previewed.

#### Custom resources {#custom-resources-6}

* Fixed an error that could lead to a server crash if a custom resource contained a field with a dynamic default value.
* Fixed an error caused by moving, then deleting an element in the **[!UICONTROL Detail screen configuration]** section while defining screens of a custom resource.
* Fixed an error that occurred when a default value had been defined for an **integer** list that did not include **0** in its range of possible values.
* Fixed an error that could prevent an element from being added in the detail screen configuration of a custom resource after a reinitialization.

#### Workflows {#workflows-6}

* Fixed an error that could cause logs of all activities in a workflow to be displayed instead of only displaying those of the activity selected.
* Fixed an error in the **[!UICONTROL Scheduler]** activity. The **[!UICONTROL Day of the month]** option was not correctly taken into account and replaced by **[!UICONTROL Week day]** .
* Fixed an error that could prevent a **[!UICONTROL Scheduler]** activity from working correctly with the expiration mode set to **[!UICONTROL After a certain number of iterations]** .
* Fixed an error that occurred when exporting data using an **[!UICONTROL Extract file]** activity. The number of lines present in the export file was inferior to the number of exported elements.
* Fixed an error that could prevent a file in a **[!UICONTROL Load file]** activity from being selected.
* Fixed an error that prevented fields that were to be updated in an **[!UICONTROL Update data]** activity from being deleted.
* Fixed an error that prevented the modifications made to a workflow from being saved after having opened the workflow execution logs.
* Fixed an error that caused a **[!UICONTROL Load file]** activity to be executed twice if it was configured to use the file from its inbound transition and this file had been loaded using a **[!UICONTROL Transfer file]** activity.
* Fixed an error that could prevent certain temporary entities from being correctly processed by an **Exclusion** activity.
* Fixed an error that could prevent a **[!UICONTROL Query]** activity from being executed correctly if the targeting dimension and the filtering dimension configured in the activity were different.
* Fixed an error concerning the automatic naming of outbound transitions added to a **[!UICONTROL Fork]** activity that could prevent the workflow from being saved.

#### Content editing {#content-editing-2}

* Fixed an error that could lead to an icon or a search bar being undesirably displayed when editing content.

#### Landing pages {#landing-pages-3}

* Fixed an error that prevented a landing page from being imported using a package import.

#### Transactional messages {#transactional-messages-4}

* It is now possible to specify a trusted IP address in the security parameters of the Message Center Push agent operator.
* Fixed an error that could prevent a new type of event from being created.

## Release 15.11 - November 2015 {#release-15-11---november-2015}

### New capabilities {#new-capabilities-9}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> SMS Channel<br /> </td> 
   <td> You can now send SMS messages with Adobe Campaign.<br /> Just as for emails, you can create new SMS deliveries from your campaigns and from the list of marketing activities. You can also create single send and recurring SMS messages from a workflow.<br /> These SMS deliveries are based on templates that you can configure from the list of delivery templates. A default template is available.<br /> These SMS deliveries use the SMPP 3.4 protocol, used by most SMS routers.<br /> For more information, refer to the <a href="../../channels/using/about-sms-messages.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Exploring transitions<br /> </td> 
   <td> You can now explore the data and its structure in the last transition of a workflow. This allows you to check that the processes applied by each activity correspond to your needs.<br /> </td> 
  </tr> 
  <tr> 
   <td> File pre- and post-processing in workflows<br /> </td> 
   <td> You can now carry out additional processing on a data file when importing or exporting it via the <span class="uicontrol">Load file</span> and <span class="uicontrol">Extract file</span> activities.<br /> By default, you can unzip and zip a GZIP format file in these activities.<br /> For more information, refer to the documentation about the <a href="../../automating/using/load-file.md">Load file</a> and <a href="../../automating/using/extract-file.md">Extract file</a> activities.<br /> </td> 
  </tr> 
  <tr> 
   <td> Deliverability reports<br /> </td> 
   <td> An email rendering report is now available. This report allows you to view the different renderings of a message according to the support and message service used to read it.<br /> The report summary also presents the number of received messages, spam messages, unreceived messages, and messages awaiting reception.<br /> For more information, refer to the <a href="../../sending/using/email-rendering.md#email-rendering-report-description">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Package Management<br /> </td> 
   <td> It is now possible to import and export images in packages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quick actions<br /> </td> 
   <td> Certain actions appear when hovering over or after selecting an element in a list or a workflow. Some of these actions are now displayed as icons around the elements concerned in order to facilitate access. These quick actions can be used to duplicate an element, delete it, show the detail, etc.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-9}

#### General {#general-9}

* Fixed an error that could prevent access to an instance's general parameters from an administrator account.
* **Floating** data is now correctly taken into account in the custom resources.
* Fixed a display error in the list of executed simplified imports which was caused when the status of the corresponding template had been modified.

#### Landing pages {#landing-pages-4}

* Fixed certain elements of landing page templates that could be incorrectly displayed in French on English instances.

#### Audiences {#audiences}

* Fixed an error that could prevent audiences imported from Adobe Marketing Cloud from appearing in the list of audiences.
* Fixed an error that could force case-sensitivity when defining a query.
* Fixed an error that could prevent audiences from being filtered when defining a query.
* Fixed an error that could prevent an action from being canceled in an audience.

#### Workflows {#workflows-7}

* Fixed an error that could prevent the fields that were to be updated in an **[!UICONTROL Update data]** activity from manually being configured.
* Fixed an error that could cause the **[!UICONTROL Query]** activity to load infinitely when opened if the workflow had not been saved after having placed the activity in the diagram.
* Fixed an error that could cause the server to stop while counting or previewing an audience selected from a **[!UICONTROL Query]** in a workflow.
* Fixed a non-critical error that could appear when an activity in a workflow was opened.
* Fixed an error that prevented a **[!UICONTROL Scheduler]** activity from being configured to execute a workflow several times a day.
* Fixed an error that could cause fields on which you cannot carry out a query to appear in certain workflow activities.
* Fixed an error that could prevent the user from locating the KPIs added from a **[!UICONTROL Query]** on deliveries in the outbound transition.
* Fixed an error that could prevent a file audience from being created after importing a file into a workflow.
* Fixed an error that could prevent data from being updated on profiles if the **location/address3** field of the resource was used.
* Fixed an error that prevented heterogeneous collections of activities from being duplicated in a workflow.
* Fixed an error that prevented the SQL from being displayed, thus allowing errors to be diagnosed for a recurring delivery in a workflow.

#### Content editor {#content-editor-1}

* Fixed an error that would make searching in the source code of a landing page or email impossible.

#### Packages {#packages-1}

* Fixed various errors that could prevent certain types of elements from being exported in packages (particularly landing pages, workflows).
* Fixed an error that would cause the former package import label to display if the label had been modified.
* Fixed an error that could cause incompatible resources to be displayed in the list of exportable resources.

## Release 15.10 - October 2015 {#release-15-10---october-2015-}

### New capabilities {#new-capabilities-10}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Workflows: Deduplication activity<br /> </td> 
   <td> A new activity dedicated to deduplicating data is now available in the workflows. This activity allows you to filter any duplicates in your targets according to your chosen criteria.<br /> For more information, refer to the <a href="../../automating/using/deduplication.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Improved diagram<br /> </td> 
   <td> From the workflow workspace, you can now use several keyboard shortcuts to select, open, and delete activities.<br /> Activity alignment has also been improved and allows a workflow to be better visually organized.<br /> For more information, refer to the <a href="../../automating/using/workflow-interface.md#workspace">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Extract file activity<br /> </td> 
   <td> The date and time of the export is now automatically added to the labels of the files exported using an <span class="uicontrol">Extract file</span> activity. This way the files generated are unique.<br /> </td> 
  </tr> 
  <tr> 
   <td> Simplified data import<br /> </td> 
   <td> The name of the template from which a simplified import was carried out is now visible by default in the import list and in the detail of each import.<br /> </td> 
  </tr> 
  <tr> 
   <td> Custom resources<br /> </td> 
   <td> Improvement and extended possibilities for managing and defining links for custom resources.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-10}

#### Email {#email}

* Fixed an error that prevented a service unsubscription link from working correctly from a mirror page.
* Fixed an error that could prevent an email delivery label from displaying correctly on the email editing page.
* Fixed an error that could prevent an external **[!UICONTROL Routing]** account from being selected in a duplicated delivery template.

#### Audiences {#audiences-1}

* Fixed an error caused during an audience count if a 1-N link was used in the query.
* Fixed an error that could prevent a profile from being selected in an email delivery's target audience.

#### Workflows {#workflows-8}

* Fixed an error that could cause display problems when configuring an email delivery in a workflow.
* Fixed an error that could prevent the **[!UICONTROL Load file]** activity from working correctly. An blank error message would then appear.
* Fixed an error that could prevent the **[!UICONTROL Transfer file]** activity from working correctly. Access rights were not always taken into account correctly.
* Fixed an error that could prevent a file from being exported if the workflow contained a **[!UICONTROL Recurring email]** .
* Fixed an error that could prevent an email delivery from being created in a workflow or prevent the subject and the defined content from being taken into account.
* Fixed an error that could prevent a reconciliation key from being selected in an **[!UICONTROL Update data]** activity when configuring the workflow of a simplified import template.
* Fixed an error that could prevent a workflow from being saved after an activity had been deleted.

#### Platform {#platform}

* Fixed an error that could prevent a new element from being created if a custom resource contained a link to that element's resource type.
* Fixed an error that could cause a 15 minute delay for certain logs to be written.
* Fixed an error that could prevent the marketing activity list from being displayed when sorted by the **[!UICONTROL Date]** or **[!UICONTROL Indicators]** columns.

#### Landing pages {#landing-pages-5}

* Fixed an error that occurred when selecting a test profile in order to preview a landing page.

#### Transactional messages {#transactional-messages-5}

* Fixed an error that could cause the application to crash after deleting an event on a test profile.

#### Reports {#reports}

* Fixed an error that could cause incorrect data to be sent for the reports **[!UICONTROL deliveryThroughputReport]** and **[!UICONTROL deliveryTrackingReport]** .

#### Content editor {#content-editor-2}

* Fixed an HTML tag management error that occurred when processing dynamic content blocks.

## Release 15.8 - August 2015 {#release-15-8---august-2015}

### New capabilities {#new-capabilities-11}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Simplified data import<br /> </td> 
   <td> You can now import data in a simplified manner.<br /> Users simply select a template that was predefined by an administrator and upload the file containing the data to be imported. A workflow defined in the template is executed transparently for the user, who can access the details of the result of the import as well as a log of any errors.<br /> The data from these files can be inserted into the database or serve as a means to directly create an audience.<br /> For more information, refer to the <a href="../../automating/using/about-data-import-and-export.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Creating programs and campaigns<br /> </td> 
   <td> Now, campaigns and programs are configured so that the day they are created is automatically used as the start date.<br /> The end date is configured according to the start date, such as:<br /> 
    <ul> 
     <li> D+186 for programs </li> 
     <li> D+61 for campaigns </li> 
    </ul> For more information, refer to the <a href="../../start/using/programs-and-campaigns.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email<br /> </td> 
   <td> The list of tracked URLs is now read only.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional messages<br /> </td> 
   <td> You can now manage personalized transactional messages for events such as password changes or confirmations following an account being created.<br /> For more information, refer to the <a href="../../channels/using/about-transactional-messaging.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Custom resources<br /> </td> 
   <td> Several functionalities added such as: extending a test profile, status management, and deleting resources.<br /> For more information, refer to the <a href="../../developing/using/resource-statuses.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-11}

#### Display {#display}

* Fixed an error that could lead to two fields being juxtaposed in the query editor in Safari.

#### Content editor {#content-editor-3}

* Fixed an error that prevented the characters '<', '&', and '>' from being used in an email subject.

#### Email {#email-1}

* Fixed an error that prevented the user from adding text after dynamic text.

#### Lists {#lists}

* Fixed an error that prevented the **Message** column in workflow execution logs from being exported correctly.

#### Profiles and audiences {#profiles-and-audiences}

* Fixed an error that lead to a double confirmation of when an element was duplicated or deleted. **Hybrid devices using Internet Explorer 11 only**.

#### Workflows {#workflows-9}

* Fixed an error that could prevent emails from being sent from a workflow.
* Fixed an error that could prevent a workflow from executing when the name of the rejection file was not specified in a **[!UICONTROL Load file]** activity.
* Fixed an error that could prevent a workflow from executing when the **[!UICONTROL Execution frequency]** of a **[!UICONTROL Schedule]** activity was set to **[!UICONTROL Daily]** .

#### Platform {#platform-1}

* Fixed an error that prevented thumbnails from being generated in a load balanced environment.

## Release 15.7 - July 2015 {#release-15-7---july-2015}

### New capabilities {#new-capabilities-12}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Exporting lists<br /> </td> 
   <td> You can now export content from your lists into a file in CSV format. This function is available in all screens with a <strong>List</strong> mode (for example: profile list).<br /> The data exported is the data in the columns displayed when exporting. By editing the list, you can therefore select the data that you would like to export.<br /> For more information on using this functionality, refer to the <a href="../../automating/using/exporting-lists.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration with Adobe Profiles &amp; Audiences<br /> </td> 
   <td> You can now share audiences between Adobe Campaign and your other Adobe Marketing Cloud solutions:<br /> 
    <ul> 
     <li> Export: when you save an audience composed of profiles in a workflow, a new <span class="uicontrol">Share in Adobe Marketing Cloud</span> option allows you to add profiles to an existing audience or to create a new audience. </li> 
     <li> Import: by creating a <strong>List</strong> type audience from the audience management screen, a new option allows you to identify it as an <span class="uicontrol">Adobe Marketing Cloud Audience</span> . You can then select an existing shared audience to import it into Adobe Campaign. </li> 
    </ul> For more information on configuring and using this functionality, refer to the <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor - Dynamic content<br /> </td> 
   <td> The dynamic content interface has been improved. Arrows now appear to allow you to navigate between the different dynamic contents, directly in the email body.<br /> For more information on using this functionality, refer to the <a href="../../designing/using/personalization.md#defining-dynamic-content-in-an-email">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor - Dynamic text<br /> </td> 
   <td> From the content editor of an email, you can now define dynamic text:<br /> 
    <ul> 
     <li> in an email subject, </li> 
     <li> in HTML mode, </li> 
     <li> or in Text mode. </li> 
    </ul> For more information on using this functionality, refer to the <a href="../../channels/using/defining-dynamic-text.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Programs and campaigns - Reports<br /> </td> 
   <td> The interface and graphics of the reports have been improved.<br /> For more information on using this functionality, refer to the <a href="../../reporting/using/defining-the-report-period.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-12}

#### Installation {#installation}

* Adobe Campaign instance names are now limited to 32 characters.

#### Workflows {#workflows-10}

* Fixed an error that could prevent targeting a 'delivery' resource when editing a query in a workflow.
* Fixed an error that could prevent certain linked resources from being processed when editing a query in a workflow.
* Fixed an error that could prevent a **Recurring delivery** activity from being modified if the workflow had already been executed.

#### Emails {#emails}

* Fixed an error that prevented JavaScript syntax errors from being checked before sending an email when a dynamic content had been added via the expression editor.

#### Landing pages {#landing-pages-6}

* Fixed an error that prevented a landing page from being edited from a tablet.

#### Assets Core Service {#assets-core-service}

* When selecting a shared resource from an email or landing page that is being edited, the list of available resources is now filtered for Adobe Campaign.

## Release 15.6 - June 2015 {#release-15-6---june-2015}

### New capabilities {#new-capabilities-13}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Workflows: Reconciliation activity<br /> </td> 
   <td> A new <strong>Reconciliation</strong> activity links unidentified data (for example, after importing a file) with existing resources within a workflow.<br /> This activity is essentially used for Data Management purposes. It responds to two different use cases:<br /> 
    <ul> 
     <li> <strong>Adding relations</strong>: a <strong>Relations</strong> tab allows you to add links between inbound data and several other dimensions of the Adobe Campaign database. </li> 
     <li> <strong>Data identification</strong>: an <strong>Identification</strong> tab allows you to simply associate inbound data to columns in an existing dimension in the Adobe Campaign database. When it leaves the activity, the data is identified as belonging to the specified dimension. </li> 
    </ul> Refer to the <a href="../../automating/using/reconciliation.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Extract file activity<br /> </td> 
   <td> A new <strong>Extract file</strong> activity allows you to export data from the Adobe Campaign database in the form of an external file from a workflow. <br /> Limitation: it is currently not possible to use dynamic names for output files.<br /> Refer to the <a href="../../automating/using/extract-file.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Scheduler activity<br /> </td> 
   <td> Improved widget that allows you to select the execution time of the <strong>Scheduler</strong> activity in a workflow.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Transfer file activity<br /> </td> 
   <td> SFTP is now supported.<br /> </td> 
  </tr> 
  <tr> 
   <td> Custom resources<br /> </td> 
   <td> The <span class="uicontrol">Development</span> menu now allows users with admin rights to enrich the data templates provided by creating their own custom resources, such as purchase or product tables. <br /> Out-of-the-box resources can also be extended in order to add new fields to them.<br /> In addition, navigation in the screens corresponding to new or extended custom resources can be configured.<br /> Refer to the <a href="../../developing/using/data-model-concepts.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Test profiles<br /> </td> 
   <td> The <strong>Middle name</strong> and <strong>Title</strong> of the test profiles can now be selected when configuring the list of test profiles.<br /> </td> 
  </tr> 
  <tr> 
   <td> Content editor: Dynamic content<br /> </td> 
   <td> You can define different contents which will be displayed dynamically to the user according to the conditions defined via the expression editor.<br /> Refer to the <a href="../../designing/using/personalization.md#defining-dynamic-content-in-an-email">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email<br /> </td> 
   <td> A <strong>Test profiles</strong> column is now available in an email's sending logs.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-13}

#### Lists {#lists-1}

* Deleting an element from a list now results in the list being automatically refreshed.
* Fixed an error that prevented elements from being selected from a list containing only one column.
* Fixed an error that caused changes applied to the display of a list to be lost after refreshing the page.
* Both the middle name and the title of test profiles can now be displayed in the test profile list.
* Fixed an error that occurred when selecting a checkbox in a list with Mozilla Firefox.

#### Audiences {#audiences-2}

* Fixed an error that prevented the **[!UICONTROL Add]** button from being used in the audience interface.

#### Emails {#emails-1}

* Fixed a JavaScript error that prevented the preview button from being used twice in a row when editing an email.
* Fixed an error that prevented the **[!UICONTROL Edit properties]** and **[!UICONTROL Show proofs]** buttons from being used on Microsoft Surface Pro3 tablets using Internet Explorer 11.
* Fixed an error that could prevent an email's sending logs from being displayed.

#### Landing pages {#landing-pages-7}

* Fixed an error that prevented the **Brand logo** content block from being used when editing content in a landing page. 
* Fixed an error that prevented landing pages from being displayed in the marketing activity list if validity dates were specified for the landing page.

#### Workflows {#workflows-11}

* Fixed an error that prevented limiting a segment in group mode from working correctly when configuring a **Segmentation** activity. 
* Fixed an error that prevented a transition from being selected after having configured a **Segmentation** activity.
* Fixed an error that prevented a transition from being deleted after having configured a **Segmentation** activity.
* Fixed an error that prevented populations from being counted and previewed within a **Segmentation** activity.
* Fixed an error that prevented a recurring email from being effectively deleted.
* Fixed an error that caused data from a deleted **Transfer file** activity to appear in a new **Transfer file** activity. 
* Fixed an error that prevented an exclusion rule from being correctly taken into account within an **Exclusion** activity.
* Fixed an error that occurred when deleting an email delivery activity in a workflow. The corresponding deliveries are now also removed from the marketing activity list.

#### Navigation {#navigation}

* You can now use the tab key to properly navigate between fields on the same page.

## Release 15.4 - April 2015 {#release-15-4---april-2015}

### New capabilities {#new-capabilities-14}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Package exports / Package imports<br /> </td> 
   <td> The <strong>Deployment</strong> menu now allows users with admin rights to exchange resources between different Adobe Campaign instances by exporting and importing packages.<br /> Refer to the <a href="../../automating/using/managing-packages.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Reports<br /> </td> 
   <td> All reports (except the <strong>Hot clicks</strong> report) can now be accessed from a program. These reports are:<br /> 
    <ul> 
     <li> Program delivery throughput </li> 
     <li> Program tracking indicators </li> 
     <li> Program breakdown by domain </li> 
     <li> Program non-deliverables and bounces </li> 
     <li> Program URLs and click streams </li> 
    </ul> These reports can be filtered over a given period (e.g. three months, six months, etc.). The campaign reports can also be filtered.<br /> Refer to the <a href="../../reporting/using/about-dynamic-reports.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: <strong>Email delivery</strong> activity<br /> </td> 
   <td> The <strong>Email delivery</strong> activity in the workflows has been improved. You can now find emails, recurring emails, and detailed information regarding recurring email executions from the list of application marketing activities.<br /> Refer to the <a href="../../automating/using/email-delivery.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: <strong>Segmentation</strong> activity<br /> </td> 
   <td> The <strong>Segmentation</strong> activity is now available in the workflows. This activity allows you to create one or several segments and link a segment code to them from a population computed by activities placed upstream in the same workflow. From this activity, the segments can be processed in one single transition or in different multiple transitions. There are now options to filter the population and limit the size of each segment to optimize personalization. For example, you can randomly select profiles that correspond to specific criteria.<br /> Refer to the <a href="../../automating/using/segmentation.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integrations: <strong>Assets Core Service</strong><br /> </td> 
   <td> You can now use shared resources via <strong>Assets Core Service</strong> in your email and landing page contents. You can manage your shared resources directly from Adobe Marketing Cloud.<br /> Refer to the <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integrations: <strong>Adobe Target</strong><br /> </td> 
   <td> You can now insert images that are dynamically computed by <strong>Adobe Target</strong> into your Adobe Campaign emails. This allows you to offer several versions of the same email by personalizing the content according to the criteria defined in Adobe Target segments.<br /> Refer to the <a href="../../integrating/using/about-campaign-target-integration.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor: <strong>Block selector</strong><br /> </td> 
   <td> When a block is selected in the HTML content editor, a breadcrumb is displayed at the bottom of the editing zone. This allows you to easily navigate to and select different elements.<br /> Refer to the <a href="../../channels/using/designing-a-landing-page.md#managing-landing-page-structure-and-style">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Release 15.3 - March 2015 {#release-15-3---march-2015}

### New capabilities {#new-capabilities-15}

<table> 
 <thead> 
  <tr> 
   <th> Functionality<br /> </th> 
   <th> Description<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Reports<br /> </td> 
   <td> The reports can now be accessed directly from a program or a campaign. The <strong>Delivery summary</strong> report has been added at a program level.<br /> Refer to the <a href="../../reporting/using/delivery-summary.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Update data<br /> </td> 
   <td> In the workflows, the available <strong>Update data</strong> activity has a new option, which allows you to automatically link inbound data fields with the fields of an application schema. This helps facilitate the selection process for updating fields.<br /> Refer to the <a href="../../automating/using/update-data.md">detailed documentation</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Email delivery<br /> </td> 
   <td> In workflows, the advanced options of the <strong>Email delivery</strong> activity can now be accessed via a specific button in the action bar. This button is only available if an <strong>Email delivery</strong> activity is selected. The main benefit is that it allows you to add an outbound transition to the activity and to edit the name of the activity as it is displayed in the workflow.<br /> Refer to the <a href="../../automating/using/email-delivery.md">detailed documentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Patches {#patches-14}

#### General {#general-10}

* Fixed an error that prevented the recipient from being displayed when creating a delivery.
* Fixed an error that prevented an audience that was based on a 'Recipients who have opened' condition from being used.
* Fixed an error that prohibited an empty profile from being deleted.
* Fixed an error which occurred when previewing a delivery.
* Fixed an error that prevented a marketing activity from being duplicated.
* Fixed an error that occurred when deleting a campaign.

