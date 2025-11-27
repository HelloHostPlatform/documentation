# Connectors

Several components of HelloHost are provided with the help of third party connections. API keys and configuration are required here.

## Payments

Currently the only supported payment provider for HelloHost is **Mollie**. If you want to allow users to pay invoices directly, an account here will be required.

HelloHost supports payment links to any of your activated payment methods and direct debit payments with SEPA transfers or credit cards.

More information about Mollie can be found here: [https://www.mollie.com](https://www.mollie.com)

### Mollie Setup

1. Create an account at [Mollie.com](https://www.mollie.com)
2. Complete the onboarding process and verify your business
3. Navigate to Developers > API Keys in your Mollie dashboard
4. Copy your API key (Live or Test)
5. Enter the API key in HelloHost Settings > Payments

### Supported Payment Methods

* **iDEAL** - Popular in the Netherlands
* **Credit Card** - Visa, Mastercard, American Express
* **SEPA Direct Debit** - Automated recurring payments
* **PayPal** - International payments
* **Bancontact** - Popular in Belgium
* **Sofort** - European bank transfers
* **Apple Pay** - Mobile payments
* **Google Pay** - Mobile payments
* And many more supported by Mollie

### Features

* **Payment Links** - Generate payment links for invoices
* **Subscription Billing** - Automated recurring payments via Laravel Cashier
* **Refunds** - Process full and partial refunds
* **Mandates** - SEPA direct debit mandate management
* **Webhooks** - Real-time payment status updates
* **Multi-currency** - Support for multiple currencies

## Domain Registrars

HelloHost supports several domain registrars. We recommend using OXXA for the best experience.

### OXXA

OXXA provides a big selection of domain TLDs available for direct registration. An account on their platform is required to use the connection.

More information about OXXA can be found here: [https://www.oxxa.com/](https://www.oxxa.com/)

**Supported features:**

* Domain listing - View all registered domains
* Domain registration - Register new domains
* Domain transfer - Transfer domains from other registrars
* DNS management - Full DNS zone editing (A, AAAA, CNAME, MX, TXT, etc.)
* Domain locking - Lock/unlock domains
* Auth codes - Request EPP/auth codes for transfers
* Auto-renewal management - Enable/disable auto-renewal
* Contact management - Update domain contacts
* WHOIS privacy - Enable WHOIS privacy protection

**Setup:**

1. Create a reseller account at OXXA
2. Obtain your API credentials from the OXXA dashboard
3. Enter the API credentials in HelloHost Settings > Domain Registrars
4. Test the connection and start managing domains

### Versio

We provide limited support for Versio. An account on their platform is required to use the connection.

More information: [https://www.versio.nl/](https://www.versio.nl/)

**Supported features:**

* Domain listing - View registered domains
* Auto-renewal management - Enable/disable auto-renewal

**Setup:**

1. Create a reseller account at Versio
2. Obtain API credentials
3. Configure in HelloHost Settings > Domain Registrars

**Note:** Versio integration has limited functionality compared to OXXA. For full domain management features, we recommend using OXXA.

## Hosting Servers

We provide support for several of the more common hosting management platforms. This feature is currently under development and being extended. In order to use these connections you will either need a server or reseller account, and an API key to connect the servers directly.

### cPanel

cPanel is one of the most popular web hosting control panels.

More information: [https://cpanel.net/](https://cpanel.net/)

**Supported features:**

* Create accounts - Automatically provision hosting accounts
* Delete accounts - Remove hosting accounts
* Account management - Basic account operations

**Setup:**

1. Ensure you have WHM (Web Host Manager) access
2. Generate an API token in WHM
3. Add server connection in HelloHost Settings > Hosting Servers
4. Configure cPanel as the server type
5. Enter server hostname and API credentials

**Requirements:**
* WHM root access or reseller account
* API token authentication enabled
* HTTPS access to WHM API

### DirectAdmin

DirectAdmin is a lightweight and fast web hosting control panel.

More information: [https://www.directadmin.com/](https://www.directadmin.com/)

**Supported features:**

* Create accounts - Automatically provision hosting accounts
* Delete accounts - Remove hosting accounts

**Setup:**

1. Ensure you have DirectAdmin admin or reseller access
2. Generate API credentials
3. Add server connection in HelloHost Settings > Hosting Servers
4. Configure DirectAdmin as the server type
5. Enter server details and credentials

**Requirements:**
* Admin or reseller level access
* API access enabled
* HTTPS access to DirectAdmin

## File Storage

### Amazon S3

HelloHost supports Amazon S3 for scalable and reliable file storage.

More information: [https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)

**Features:**

* **Scalable Storage** - Unlimited storage capacity
* **High Availability** - 99.99% uptime SLA
* **Secure** - Encrypted at rest and in transit
* **Cost-effective** - Pay only for what you use
* **Multi-region** - Store files close to your users

**Supported File Types:**

* Client attachments
* Invoice PDFs
* Service images
* Task attachments
* Backups

**Setup:**

1. Create an AWS account
2. Create an S3 bucket in your preferred region
3. Create an IAM user with S3 access
4. Generate access keys for the IAM user
5. Configure S3 credentials in HelloHost environment settings
6. Set bucket name and region

**Required Permissions:**

* `s3:PutObject` - Upload files
* `s3:GetObject` - Download files
* `s3:DeleteObject` - Delete files
* `s3:ListBucket` - List bucket contents

## Email Delivery

### Postmark

For reliable transactional email delivery, HelloHost integrates with Postmark.

More information: [https://postmarkapp.com/](https://postmarkapp.com/)

**Features:**

* **High Deliverability** - Optimized for transactional emails
* **Fast Delivery** - Emails delivered in seconds
* **Detailed Analytics** - Open rates, bounce tracking, spam complaints
* **Email Templates** - Use Postmark's template system
* **Webhook Support** - Real-time delivery notifications

**Supported Email Types:**

* Invoice notifications
* Payment confirmations
* Order notifications
* Task updates
* Account activation emails
* Password resets
* Custom notifications

**Setup:**

1. Create a Postmark account
2. Create a server in Postmark
3. Verify your sending domain
4. Copy your Server API Token
5. Configure in HelloHost Settings > Mail
6. Select Postmark as your mail driver

## Translation Services

### DeepL

HelloHost integrates with DeepL for high-quality automated translations in the ticket workflow.

More information: [https://www.deepl.com/](https://www.deepl.com/)

**Setup:**

1. Create a DeepL API account
2. Subscribe to a plan (Free or Pro)
3. Copy your API authentication key
4. Configure in HelloHost environment settings
5. Use translation features in content management

## Performance Monitoring

### Google Lighthouse

HelloHost integrates with Google Lighthouse for website performance monitoring through the Solutionsio service.

**Features:**

* **Performance Scores** - Overall website performance metrics
* **Desktop & Mobile** - Separate scores for different devices
* **Historical Tracking** - Track performance changes over time
* **Multiple Metrics:**
  * Performance
  * Accessibility
  * Best Practices
  * SEO
* **Automated Syncing** - Regular performance data updates

**Use Cases:**

* Monitor client website performance
* Track improvements after optimizations
* Report on hosting service quality
* Identify performance issues proactively

**Setup:**

1. Contact solutions.io for API access
2. Obtain API credentials
3. Configure in HelloHost settings
4. Add PageSpeed reports for client websites
5. Reports will sync automatically

## Configuration

All connector configurations can be managed in the HelloHost settings panel:

1. Log in to your HelloHost admin account
2. Navigate to Settings from the account menu
3. Select the appropriate section (Payments, Domain Registrars, Hosting Servers, etc.)
4. Enter your API credentials and configuration
5. Test the connection to verify setup
6. Save and activate the integration

## Troubleshooting

### Connection Issues

If you experience connection problems:

* **Verify API credentials** - Ensure keys are copied correctly
* **Check API permissions** - Verify your account has necessary permissions
* **Test API endpoint** - Confirm the service is accessible from your server
* **Review firewall rules** - Ensure outbound connections are allowed
* **Check service status** - Verify the third-party service is operational

### API Limits

Most services have API rate limits:

* **Mollie** - Generous limits for most operations
* **OXXA** - Rate limits vary by operation type
* **Versio** - Conservative rate limits
* **DeepL** - Character limits based on subscription

Monitor your usage to avoid hitting limits. HelloHost will handle rate limiting gracefully and queue operations when necessary.
