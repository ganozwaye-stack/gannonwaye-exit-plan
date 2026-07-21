# Automations

> Scheduled and event-triggered automations to rebuild

## Scheduled Automations

| Name | Schedule | Function | Description |
|------|----------|----------|-------------|
| Daily Revenue Email Summary | 7am AEST daily | `sendDailyRevenueSummary` | Sends revenue/profit/top merch email |
| Fan Reminder Sender | Every 5 min | `sendFanReminders` | Sends due fan reminder emails |
| Cleanup Old Notifications | Daily | `cleanupOldNotifications` | Removes old read notifications |
| Birthday Discounts | Daily | `sendBirthdayDiscount` | Sends birthday discount emails |
| Agent Intelligence Loop | Scheduled | `agentIntelligenceLoop` | Runs agent intelligence cycle |
| Agent Proposal Scanner | Scheduled | `agentProposalScanner` | Scans for agent action proposals |
| Agent Self-Improvement | Scheduled | `agentSelfImprovement` | Agent self-improvement cycle |
| Executive Morning Brief | 7am | `executiveMorningBrief` | Generates morning brief |
| Autonomous Trend Engine | Scheduled | `autonomousTrendEngine` | Trend detection |
| Autonomous Alert System | Scheduled | `autonomousAlertSystem` | Alert monitoring |
| Automated Site Tests | Scheduled | `automatedSiteTests` | Runs automated tests |
| Social Comment Monitor | Scheduled | `socialCommentMonitor` | Monitors social comments |

## Entity-Triggered Automations

| Entity | Event | Function | Description |
|--------|-------|----------|-------------|
| MerchOrder | Create | `onNewOrderAutomation` | Processes new order |
| MerchOrder | Create | `onNewOrderAlert` | Sends order alert |
| MerchOrder | Create | `onNewOrderSlack` | Posts to Slack |
| MerchOrder | Create | `notifyAdminNewOrder` | Notifies admin |
| MerchOrder | Create | `syncOrderToSheets` | Syncs to Google Sheets |
| EmailSubscriber | Create | `onNewSubscriberWelcome` | Welcome flow |
| EmailSubscriber | Create | `welcomeNewSubscriber` | Welcome email |
| ApprovalQueueItem | Create | `onNewApprovalItem` | Approval notification |
| AdminNotification | Create | (various) | Notification routing |

## Connector Webhook Automations

| Connector | Event | Function |
|------------|-------|----------|
| Google Calendar | events | `onCalendarEvent` |
| Google Drive | changes | `onDriveChange` |
| Gmail | mailbox | (email processing) |
| Slack | message | (Slack message handling) |
| Instagram | (webhooks) | `onNewMerchInstagram` |
| TikTok | (webhooks) | `tiktokWebhook` |
| Stripe | (webhooks) | `stripeWebhook` |
| HeyGen | (webhooks) | `heygenWebhook` |

## Migration Notes

- On Emergent, rebuild using Emergent's automation/cron system
- Scheduled tasks: use cron jobs or scheduled functions
- Entity triggers: use database triggers or event listeners
- Webhooks: register new webhook URLs with each provider after deploy
