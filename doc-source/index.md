# Amazon Pinpoint Developer Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is Amazon Pinpoint?](welcome.md)
+ [Tutorials](tutorials.md)
   + [Tutorial: Using Postman with the Amazon Pinpoint API](tutorials-using-postman.md)
      + [Prerequisites](tutorials-using-postman-prerequisites.md)
      + [Step 1: Create IAM policies and roles](tutorials-using-postman-iam-user.md)
      + [Step 2: Set up Postman](tutorials-using-postman-configuration.md)
      + [Step 3: Send additional requests](tutorials-using-postman-sample-requests.md)
   + [Tutorial: Importing data into Amazon Pinpoint from external sources](tutorials-importing-data.md)
      + [Prerequisites](tutorials-importing-data-prereqs.md)
      + [Step 1: Create an Amazon S3 bucket](tutorials-importing-data-create-s3-bucket.md)
      + [Step 2: Create IAM roles](tutorials-importing-data-create-iam-roles.md)
      + [Step 3: Create a package that contains the required Python libraries](tutorials-importing-data-create-python-package.md)
      + [Step 4: Create the Lambda function that splits input data](tutorials-importing-data-lambda-function-input-split.md)
      + [Step 5: Create the Lambda function that processes the incoming records](tutorials-importing-data-lambda-function-process-incoming.md)
      + [Step 6: Create the Lambda function that imports records into Amazon Pinpoint](tutorials-importing-data-lambda-function-import-job.md)
      + [Step 7: Set up Amazon S3 events](tutorials-importing-data-s3-events.md)
      + [Next steps](tutorials-importing-data-next-steps.md)
   + [Tutorial: Setting up an email preference management system](tutorials-email-prefs.md)
      + [Prerequisites](tutorials-email-prefs-prereqs.md)
      + [Step 1: Set Up Amazon Pinpoint](tutorials-email-prefs-part-1.md)
      + [Step 2: Add or configure endpoints](tutorials-email-prefs-part-2.md)
      + [Step 3: Create IAM policies and roles](tutorials-email-prefs-part-3.md)
      + [Step 4: Create the Lambda function](tutorials-email-prefs-part-4.md)
      + [Step 5: Set up Amazon API Gateway](tutorials-email-prefs-part-5.md)
      + [Step 6: Create and deploy the web form](tutorials-email-prefs-part-6.md)
      + [Step 7: Create and send Amazon Pinpoint campaigns](tutorials-email-prefs-part-7.md)
      + [Next steps](tutorials-email-prefs-next-steps.md)
   + [Tutorial: Setting up an SMS registration system](tutorials-two-way-sms.md)
      + [Prerequisites](tutorials-two-way-sms-prereqs.md)
      + [Step 1: Set up Amazon Pinpoint](tutorials-two-way-sms-part-1.md)
      + [Step 2: Create IAM policies and roles](tutorials-two-way-sms-part-2.md)
      + [Step 3: Create Lambda functions](tutorials-two-way-sms-part-3.md)
      + [Step 4: Set up Amazon API Gateway](tutorials-two-way-sms-part-4.md)
      + [Step 5: Create and deploy the web form](tutorials-two-way-sms-part-5.md)
      + [Next steps](tutorials-two-way-sms-next-steps.md)
+ [Integrating Amazon Pinpoint with your application](integrate.md)
   + [AWS SDK support for Amazon Pinpoint](integrate-supported-sdks.md)
   + [Integrating the AWS mobile SDKs or JavaScript library with your application](integrate-sdk.md)
   + [Registering endpoints in your application](integrate-endpoints.md)
   + [Reporting events in your application](integrate-events.md)
   + [Handling push notifications](integrate-push.md)
      + [Setting up push notifications for Amazon Pinpoint](mobile-push.md)
         + [Setting up iOS push notifications](apns-setup.md)
         + [Setting up Android push notifications](mobile-push-android.md)
         + [Create a project in Amazon Pinpoint](mobile-push-create-project.md)
      + [Handling push notifications](integrate-push-services.md)
+ [Defining your audience to Amazon Pinpoint](audience-define.md)
   + [Adding endpoints to Amazon Pinpoint](audience-define-endpoints.md)
   + [Associating users with Amazon Pinpoint endpoints](audience-define-user.md)
   + [Adding a batch of endpoints to Amazon Pinpoint](audience-define-endpoints-batch.md)
   + [Importing endpoints into Amazon Pinpoint](audience-define-import.md)
   + [Deleting endpoints from Amazon Pinpoint](audience-define-remove.md)
+ [Accessing audience data in Amazon Pinpoint](audience-data.md)
   + [Looking up endpoints with Amazon Pinpoint](audience-data-endpoints.md)
   + [Exporting endpoints from Amazon Pinpoint](audience-data-export.md)
   + [Listing endpoint IDs with Amazon Pinpoint](audience-data-list-ids.md)
+ [Creating segments](segments.md)
   + [Building segments](segments-dimensional.md)
   + [Importing segments](segments-importing.md)
   + [Customizing segments with AWS Lambda](segments-dynamic.md)
+ [Creating campaigns](campaigns.md)
+ [Validating phone numbers in Amazon Pinpoint](validate-phone-numbers.md)
+ [Sending transactional messages from your apps](send-messages.md)
   + [Send transactional email messages](send-messages-email.md)
      + [Send email by using the Amazon Pinpoint API](send-messages-sdk.md)
      + [Send email by using the Amazon Pinpoint SMTP interface](send-messages-email-smtp.md)
   + [Send SMS messages](send-messages-sms.md)
   + [Send voice messages](send-messages-voice.md)
   + [Send push notifications](send-messages-push.md)
+ [Creating custom channels in Amazon Pinpoint](channels-custom.md)
+ [Streaming Amazon Pinpoint events to Kinesis](event-streams.md)
   + [Setting up event streaming](event-streams-setup.md)
   + [App events](event-streams-data-app.md)
   + [Campaign events](event-streams-data-campaign.md)
   + [Journey events](event-streams-data-journey.md)
   + [Email events](event-streams-data-email.md)
   + [SMS events](event-streams-data-sms.md)
+ [Querying Amazon Pinpoint analytics data](analytics.md)
   + [IAM policies for querying Amazon Pinpoint analytics data](analytics-permissions.md)
   + [Standard Amazon Pinpoint analytics metrics](analytics-standard-metrics.md)
   + [Querying Amazon Pinpoint analytics data for campaigns](analytics-query-campaigns.md)
   + [Querying Amazon Pinpoint analytics data for transactional messages](analytics-query-txn-messaging.md)
   + [Using Amazon Pinpoint analytics query results](analytics-query-results.md)
+ [Logging Amazon Pinpoint API calls with AWS CloudTrail](logging-using-cloudtrail.md)
+ [Tagging Amazon Pinpoint resources](tagging-resources.md)
+ [Customizing recommendations with AWS Lambda](ml-models-rm-lambda.md)
+ [Deleting data from Amazon Pinpoint](deleting-data.md)
+ [Security in Amazon Pinpoint](security.md)
   + [Data protection in Amazon Pinpoint](security-data-protection.md)
      + [Data encryption](security-data-protection-encryption.md)
      + [Internetwork traffic privacy](security-data-protection-internetwork-traffic.md)
   + [Identity and access management for Amazon Pinpoint](security-iam.md)
      + [How Amazon Pinpoint works with IAM](security_iam_service-with-iam.md)
      + [Amazon Pinpoint actions for IAM policies](permissions-actions.md)
      + [Amazon Pinpoint identity-based policy examples](security_iam_id-based-policy-examples.md)
      + [IAM roles for common Amazon Pinpoint tasks](security_iam_roles-common.md)
         + [IAM role for importing endpoints or segments](permissions-import-segment.md)
         + [IAM role for exporting endpoints or segments](permissions-export-endpoints.md)
         + [IAM role for retrieving recommendations from Amazon Personalize](permissions-get-recommendations.md)
         + [IAM role for streaming events to Kinesis](permissions-streams.md)
         + [IAM role for streaming email events to Kinesis Data Firehose](permissions-stream-email-events-kinesis.md)
      + [Troubleshooting Amazon Pinpoint identity and access management](security_iam_troubleshoot.md)
   + [Logging and monitoring in Amazon Pinpoint](security-incident-response.md)
   + [Compliance validation for Amazon Pinpoint](security-compliance-validation.md)
   + [Resilience in Amazon Pinpoint](security-disaster-recovery-resiliency.md)
   + [Infrastructure security in Amazon Pinpoint](security-infrastructure-security.md)
   + [Configuration and vulnerability analysis in Amazon Pinpoint](security-vulnerability-analysis-management.md)
+ [Amazon Pinpoint quotas](quotas.md)
+ [Document history for Amazon Pinpoint](doc-history.md)