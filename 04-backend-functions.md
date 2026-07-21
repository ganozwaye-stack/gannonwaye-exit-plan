# Backend Functions

> 115 backend functions to rebuild on the new platform

## By Category

## Payments
### `stripeWebhook`
Receives Stripe webhook events, creates/updates orders

### `createCheckoutSession`
Creates Stripe Checkout Session for cart checkout

### `createPaymentIntent`
Creates Stripe Payment Intent for direct payment

### `validatePromoCode`
Validates promo code rules, exclusions, usage limits

### `calculateShippingRate`
Calculates shipping based on rules and destination

### `stripeIntelligenceRouter`
Routes Stripe events to appropriate handlers

### `recoverStripeOrders`
Recovers orders from Stripe if webhook missed

### `getStripeConfig`
Returns Stripe publishable key for frontend

### `applyCheckoutDiscountGuard`
Enforces discount rules at checkout

### `recordPromoUsage`
Records promo code usage and increments count

### `testCheckoutMath`
Tests checkout calculation accuracy

### `orderLockingMiddleware`
Deduplication via order locks

## Orders
### `fulfilOrderAndNotify`
Marks order fulfilled, sends notifications

### `notifyAdmin`
Sends admin notification for new order

### `notifyAdminNewOrder`
Admin alert for new order (email)

### `notifyAdminNewOrderGmail`
Admin alert for new order (Gmail)

### `onNewOrderAlert`
Triggers alert chain on new order

### `onNewOrderAutomation`
Automated order processing on creation

### `onNewOrderSlack`
Posts new order to Slack channel

### `sendOrderReceipt`
Sends order receipt to customer

### `syncOrderNotifications`
Syncs order status across notification channels

### `syncOrderToSheet`
Syncs order to Google Sheet

### `syncOrderToSheets`
Syncs order to Google Sheets (plural)

### `onOrderShipped`
Triggers shipped notifications

### `orderAlertEmail`
Sends order alert email

## Email
### `welcomeEmail`
Sends welcome email to new subscriber

### `welcomeNewSubscriber`
Welcome flow for new subscribers

### `sendFanReminders`
Sends scheduled fan reminder emails

### `sendGiftEmail`
Sends gift card email to recipient

### `sendGiftOfferEmail`
Sends gift offer promotional email

### `sendPromoCodeEmails`
Distributes promo codes via email

### `sendRevealNewsletter`
Sends reveal newsletter campaign

### `sendBirthdayDiscount`
Sends birthday discount to customers

### `sendWelcomeEmailGmail`
Welcome email via Gmail connector

### `sendDailyRevenueSummary`
Daily 7am revenue/profit email summary

## AI/Content
### `generateResearchedSocialContent`
Generates web-researched social content

### `generateContentPost`
Generates a social content post

### `generateDailyDrafts`
Generates daily content drafts

### `generateReleaseSprint`
Generates release sprint plan

### `generatePresaveLinks`
Generates pre-save links for releases

### `generateDonorReceipt`
Generates donor receipt document

### `generateTaxInvoice`
Generates tax invoice PDF

### `openaiAgent`
OpenAI agent handler

### `openAIContentAssistant`
OpenAI content writing assistant

### `openAIMessageRouter`
Routes messages to OpenAI

### `openAIQAAssistant`
OpenAI QA testing assistant

### `openAIRepairAssistant`
OpenAI code repair assistant

### `openAIStoreConversionAssistant`
OpenAI store conversion assistant

### `openAIVideoAssistant`
OpenAI video production assistant

## Social
### `postToInstagram`
Posts content to Instagram

### `postApprovedToTiktok`
Posts approved content to TikTok

### `scheduledSocialPost`
Executes a scheduled social post

### `autonomousSocialPoster`
Autonomous social media posting agent

### `socialCommentMonitor`
Monitors social comments

### `socialQualityCouncil`
Reviews social content quality

### `tiktokOAuth`
TikTok OAuth flow handler

### `tiktokUploadDraft`
Uploads TikTok draft video

### `tiktokWebhook`
TikTok webhook event handler

## Metricool
### `metricoolSchedulePost`
Schedules post via Metricool API

### `metricoolImportMetrics`
Imports analytics from Metricool

### `metricoolNormalizeMedia`
Normalizes media for Metricool

### `metricoolDiagnostics`
Metricool integration diagnostics

### `listMetricoolProfiles`
Lists Metricool profiles

### `validateMetricoolConfig`
Validates Metricool configuration

## Agents
### `agentIntelligenceLoop`
Main agent intelligence loop

### `agentProposalScanner`
Scans agent action proposals

### `agentSelfImprovement`
Agent self-improvement cycle

### `seedAgentRegistry`
Seeds agent registry with known agents

## Health
### `runSiteHealthCheck`
Runs comprehensive site health check

### `integrationHealthCheck`
Checks all integration health

### `automatedSiteTests`
Runs automated site tests

### `shippingOptimisationAudit`
Audits shipping rate rules

## Calendar
### `onCalendarEvent`
Handles Google Calendar webhook events

### `releaseCalendarSync`
Syncs releases to Google Calendar

### `releaseCountdownBrief`
Generates release countdown brief

### `syncGoogleCalendar`
Full Google Calendar sync

## Community
### `communityReplyHandler`
Handles community reply submissions

### `aiFanReply`
AI-generated fan reply

### `fanPostNotification`
Notifies on new fan post

### `fanMediaSubmissionEmail`
Email on fan media submission

## Notifications
### `notifyAdminBookingEnquiry`
Admin notification for booking enquiry

### `notifyAdminLowStock`
Admin alert for low stock

### `notifyInterestRegistration`
Notifies on merch interest registration

### `notifySubscribersNewRelease`
Emails subscribers about new release

### `onNewApprovalItem`
Triggers on new approval queue item

### `onNewSubscriberWelcome`
Triggers welcome flow on new subscriber

### `sendSlackAlert`
Sends alert to Slack

### `autonomousAlertSystem`
Autonomous alert monitoring

### `autonomousTrendEngine`
Autonomous trend detection

### `autonomousResearch`
Autonomous research agent

## HeyGen
### `generateHeyGenVideo`
Creates HeyGen avatar video

### `createHeygenPhotoAvatar`
Creates HeyGen photo avatar

### `registerHeygenWebhook`
Registers HeyGen webhook URL

### `heygenWebhook`
HeyGen webhook event handler

## Drive
### `listDriveFiles`
Lists Google Drive files

### `onDriveChange`
Handles Google Drive webhook

## Other
### `collectReleaseFeedback`
Collects release feedback

### `executiveMorningBrief`
Generates executive morning brief

### `growthOpportunityScanner`
Scans for growth opportunities

### `onMemorySubmission`
Handles memorial memory submissions

### `onNewMerchInstagram`
Posts new merch to Instagram

### `proofApprovalChain`
Manages proof approval chain

### `publishApprovedProposal`
Publishes approved agent proposal

### `publishBrandKitToGithub`
Pushes brand kit to GitHub repo

### `runSystemHealthSeed`
Seeds system health items

### `soniaChat`
Memorial chat (Sonia)

### `trackMonthlyCharityDonation`
Tracks monthly 1800RESPECT donation

### `triggerMay10Reveal`
Triggers site reveal

### `bookingWorkflowHandler`
Handles booking workflow

### `createGiftTracker`
Creates gift tracker record

### `createSampleGiftTracker`
Creates sample gift tracker

### `testCursorApiKey`
Tests Cursor API key

### `testOpenAIKey`
Tests OpenAI API key

### `cleanupOldNotifications`
Cleans up old notifications

### `automateSalesTracking`
Automates sales tracking sync

## Migration Notes

- All functions are in `base44/functions/{name}/entry.ts`
- They use Deno Deploy with the Base44 SDK
- On Emergent, these need to be rebuilt as serverless functions or API routes
- The Base44 SDK (`createClientFromRequest`) needs to be replaced with Emergent's equivalent
- Auth pattern: `const user = await base44.auth.me()` → Emergent's auth equivalent
- Service role: `base44.asServiceRole.entities.X` → Emergent's admin DB client
- Integration calls: `base44.integrations.Core.InvokeLLM/SendEmail/UploadFile/GenerateImage` → Emergent's integration layer
