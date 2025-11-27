# Configuration

Before using HelloHost there are several options that can be configured. You can find these options by hovering over your account and selecting the `Settings` link.

## General

Here you can configure your brand colors, logo's and the languages that will be available to you and your users.

### Branding
* **Brand Colors** - Set your primary and secondary brand colors
* **Logo** - Upload your company logo for emails and invoices
* **Company Name** - Display name for your organization

### Languages
* **Available Languages** - Select which languages to enable for your platform
* **Supported Languages:**
  * English (en)
  * German (de)
  * Dutch (nl)
  * Ukrainian (uk)
* **Default Language** - Set the default language for new users

## Accounts

Security and user access settings to allow users to create their own account.

### Registration Settings
* **Allow Registration** - Enable/disable public account registration
* **Email Verification** - Require email verification for new accounts
* **Default Permissions** - Set default permissions for new user accounts

### Security Settings
* **Two-Factor Authentication (2FA)** - Enable 2FA requirements for users
* **Password Requirements** - Configure password complexity rules
* **Session Timeout** - Set automatic logout duration
* **Login Attempts** - Configure failed login attempt limits

## Mail

Configure an SMTP email account to send personalized email. If you do not configure this section all email will be sent from `{brandname}@hellohost.nl` and might not be delivered correctly. You will need SMTP credentials in most cases. Certain providers require their own way of handling logins.

### SMTP Configuration
* **SMTP Host** - Your mail server hostname
* **SMTP Port** - Usually 587 (TLS) or 465 (SSL)
* **SMTP Username** - Your email account username
* **SMTP Password** - Your email account password
* **From Address** - The email address that emails will be sent from
* **From Name** - The name that will appear as the sender

### Supported Mail Providers

#### Gmail

Information to configure Google Gmail can be found here: [https://support.google.com/mail/answer/185833?hl=en](https://support.google.com/mail/answer/185833?hl=en)

**Quick Setup:**
* Host: `smtp.gmail.com`
* Port: `587` (TLS) or `465` (SSL)
* You'll need to create an App Password in your Google Account settings

#### Postmark

For reliable transactional email delivery, HelloHost supports Postmark integration.

More information: [https://postmarkapp.com](https://postmarkapp.com)

**Configuration:**
* Obtain your Postmark API token from your account
* Configure the token in your mail settings
* Enjoy high deliverability rates and detailed email tracking

#### Other SMTP Providers
HelloHost is compatible with any standard SMTP provider including:
* Microsoft 365 / Outlook
* SendGrid
* Mailgun
* Amazon SES
* Custom SMTP servers

## Invoices

Basic settings to customize your invoicing logic and basic tax information.

### Invoice Settings
* **Invoice Prefix** - Custom prefix for invoice numbers (e.g., "INV-")
* **Starting Number** - First invoice number to use
* **Due Date** - Default payment due date (e.g., 14 days)
* **Footer Text** - Custom text for invoice footer
* **Terms & Conditions** - Add terms and conditions to invoices

### Tax Configuration
* **Default Tax Rate** - Set your standard VAT/tax percentage
* **Tax Number** - Your company VAT/tax identification number
* **EU VAT Validation** - Enable automatic EU VAT number validation
* **Reverse Charge** - Configure reverse charge mechanism for B2B transactions
* **Tax-Exempt Clients** - Mark specific clients as tax-exempt

### Currency Settings
* **Default Currency** - Primary currency for your organization
* **Supported Currencies** - Enable multiple currencies for international clients
* **Exchange Rates** - Configure or update currency exchange rates

## Payments

Configure payment processing to accept online payments from clients.

### Mollie Configuration
* **Mollie API Key** - Your Mollie API key from the Mollie dashboard
* **Test Mode** - Enable test mode for development and testing
* **Webhook URL** - Automatically configured webhook for payment updates

More information: [https://www.mollie.com](https://www.mollie.com)

### Payment Methods
Enable/disable specific payment methods:
* iDEAL (Netherlands)
* Credit Card (Visa, Mastercard, American Express)
* SEPA Direct Debit
* PayPal
* Bancontact (Belgium)
* Sofort (Europe)
* Other Mollie-supported methods

### Direct Debit
* **SEPA Mandates** - Enable SEPA direct debit mandates
* **Mandate Management** - View and manage client mandates
* **Automatic Collection** - Configure automatic payment collection

## Permissions & Roles

Configure role-based access control for your team members.

### User Roles
* **Super Admin** - Full system access (cannot be restricted)
* **Admin** - Administrative access with configurable permissions
* **Employee** - Limited access based on assigned permissions
* **Client** - Customer portal access only

### Configurable Permissions

**Client Management:**
* View all clients
* Create/edit clients
* Delete clients
* Manage subscriptions
* Access password memos

**Financial Management:**
* View invoices and payments
* Create/edit invoices
* Process payments and refunds
* Manage orders
* View financial statistics

**Task Management:**
* View all tasks
* Create/edit tasks
* Assign tasks
* Review completed tasks
* Access recurring tasks

**Service Management:**
* View services
* Create/edit services
* Manage pricing
* Archive services

**System Management:**
* System settings
* User management
* Role configuration
* Integration settings

## Activity Logging

HelloHost automatically tracks user actions for security and audit purposes.

### Logged Activities
* User authentication events
* Client record changes
* Invoice creation and modifications
* Payment transactions
* Subscription changes
* Task updates
* Setting modifications
* Permission changes

### Activity Log Settings
* **Retention Period** - How long to keep activity logs
* **Log Detail Level** - Configure verbosity of logging
* **User Access** - Control who can view activity logs

## Notifications

Configure which notifications are sent to clients and team members.

### Client Notifications
* **New Invoice** - Notify clients when invoices are created
* **Invoice Reminder** - Send reminders for unpaid invoices
* **Payment Confirmation** - Confirm successful payments
* **Order Updates** - Notify about order status changes
* **Subscription Renewals** - Alert before subscription renewals
* **Domain Notifications** - Registration, transfer, and expiration alerts
* **Task Updates** - Notify clients of public task updates

### Team Notifications
* **New Orders** - Alert team when orders are placed
* **Payment Failures** - Notify of failed payment attempts
* **Task Assignments** - Notify when tasks are assigned
* **System Alerts** - Critical system notifications

### Notification Timing
* **Reminder Schedule** - Configure when to send invoice reminders
* **Renewal Notices** - Set advance notice for subscription renewals
* **Batch Processing** - Configure notification batch sending times

## Integrations

Configure third-party service integrations. See the [Connectors](connectors.md) section for detailed information.

### Available Integrations
* **Payment Providers** - Mollie for payment processing
* **Domain Registrars** - OXXA, Versio
* **Hosting Servers** - cPanel, DirectAdmin
* **Error Tracking** - Sentry for error monitoring
* **File Storage** - Amazon S3
* **Email Delivery** - Postmark
* **Translations** - DeepL
* **Performance** - Google Lighthouse (via Solutionsio)

## Advanced Settings

### Multi-tenancy
* **Tenant Domain** - Configure your tenant's custom domain
* **Database Connection** - Tenant-specific database settings (automatic)
* **Storage Path** - Tenant file storage configuration

### Performance
* **Cache Configuration** - Redis caching settings
* **Queue Workers** - Background job processing
* **Session Management** - Session driver and lifetime

### Development
* **Debug Mode** - Enable detailed error messages (development only)
* **Test Mode** - Enable test mode for integrations
* **API Access** - Generate API tokens for external integrations

### Backup & Maintenance
* **Automated Backups** - Schedule regular database backups
* **Maintenance Mode** - Enable maintenance mode for updates
* **Data Export** - Export client data and reports
