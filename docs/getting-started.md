# Getting Started

Welcome to HelloHost! This guide will help you get started with the platform.

## Creating Your Account

1. Visit [hellohost.nl](https://hellohost.nl)
2. Click **"Sign Up"** or **"Get Started"**
3. Fill in your organization details:
   * Company name
   * Your name and email
   * Choose a password
4. Verify your email address by clicking the link in the confirmation email
5. Complete the initial setup wizard

## Initial Setup

After creating your account, you'll want to configure a few essential settings to get the most out of HelloHost.

### Step 1: Configure Your Branding

Navigate to **Settings > General**:

* **Upload your logo** - This will appear on invoices and emails to clients
* **Set brand colors** - Choose colors that match your company identity
* **Select languages** - Enable the languages you and your clients will use
* **Set company details** - Add your business name and contact information

### Step 2: Setup Email

Navigate to **Settings > Mail**:

Professional emails from your own domain help build trust with clients.

**Option 1: Use Gmail**
* Host: `smtp.gmail.com`
* Port: `587`
* Create an App Password in your Google Account
* Enter your email and app password

**Option 2: Use Your Email Provider**
* Get SMTP details from your email provider
* Enter host, port, username, and password
* Set your "From" name and email address

**Option 3: Use Postmark (Recommended for high volume)**
* Sign up at [Postmark](https://postmarkapp.com)
* Get your API token
* Configure in HelloHost settings

Send a test email to make sure everything works!

### Step 3: Configure Invoicing

Navigate to **Settings > Invoices**:

* **Invoice prefix** - e.g., "INV-" for invoice numbers like INV-001
* **Starting number** - Choose your first invoice number
* **Payment terms** - Set how many days clients have to pay (e.g., 14 days)
* **Tax rate** - Set your VAT/tax percentage
* **Company details** - Add your business registration and VAT number
* **Footer text** - Add payment instructions or terms

### Step 4: Setup Payment Processing (Optional but Recommended)

To accept online payments from clients:

1. Navigate to **Settings > Payments**
2. **Sign up for Mollie** at [mollie.com](https://www.mollie.com) if you don't have an account
3. Complete Mollie's onboarding and verification process
4. Copy your API key from Mollie dashboard
5. Enter the API key in HelloHost
6. Enable your preferred payment methods (iDEAL, Credit Card, etc.)
7. Test with a small payment

With payment processing enabled, clients can pay invoices online instantly!

## Adding Your First Client

1. Click **Clients** in the main menu
2. Click the **Add Client** button
3. Fill in the client information:
   * **Basic Info**: First name, last name, company name
   * **Contact**: Email addresses for notifications and invoices, phone number
   * **Address**: Complete billing address
   * **Preferences**: Preferred language and currency
4. Click **Save**

Your client now has an account and can access their portal!

## Creating Your Service Catalog

Before you can add subscriptions, you need to create services that you offer.

1. Navigate to **Services**
2. Click **Add Service**
3. Fill in the service details:

**Basic Information:**
* **Name** - e.g., "Shared Hosting - Basic"
* **Description** - What's included in this service
* **Category** - Optional: group services into categories

**Pricing:**
* **Price** - Monthly cost
* **Billing Interval** - How often to bill (1 month, 3 months, 12 months, etc.)

**Service Type:**
* **Domain** - For domain registration services
* **Hosting** - For web hosting packages
* **Custom** - For anything else (support, SSL, email, etc.)

**Optional Settings:**
* **Featured** - Mark as a featured service for clients
* **Renewal notification** - Send notification before renewal
* **Add an image** - Make it look professional

4. Click **Save**

Repeat this for all services you want to offer.

## Adding a Subscription for a Client

Now that you have clients and services, let's add a subscription:

1. Open a client's profile
2. Go to the **Subscriptions** tab
3. Click **Add Subscription**
4. Select a service from your catalog
5. Configure the subscription:
   * **Start date** - When the subscription begins
   * **Custom price** - Override the default price if needed
   * **Auto-renewal** - Enable automatic renewal (recommended)
   * **Description** - Add specific details for this client
6. Click **Save**

HelloHost will now automatically:
* Generate invoices based on the billing cycle
* Send invoice notifications to the client
* Track renewals and send reminders

## Creating and Sending an Invoice

Invoices are usually generated automatically from subscriptions, but you can also create manual invoices:

1. Open a client's profile
2. Go to the **Invoices** tab
3. Click **Create Invoice**
4. Add invoice lines:
   * Description (e.g., "One-time setup fee")
   * Quantity
   * Unit price
   * Tax rate (automatically filled from settings)
5. Review the total
6. Click **Save & Send**

The client receives an email with:
* Professional PDF invoice
* Direct payment link (if Mollie is configured)
* Payment instructions

## Managing Support Tickets

### Creating a Task

1. Navigate to **Tasks**
2. Click **Add Task**
3. Fill in:
   * **Title** - Brief description
   * **Description** - Full details
   * **Client** - Link to client (optional)
   * **Status** - Open, In Progress, Completed
   * **Priority** - Low, Normal, High, Urgent
   * **Due date** - When it needs to be done
   * **Assign to** - Team member responsible
   * **Public** - If enabled, client can see the task
4. Click **Save**

### Converting Tasks to Invoices

Did billable work? Convert it to an invoice:

1. Open a completed task
2. Track the time spent
3. Click **Add to Invoice**
4. Select the client and invoice (or create new)
5. The task work is added as an invoice line

## Connecting Domain Registrars (Optional)

To automate domain registration and management:

### Using OXXA (Recommended)

1. Sign up for a reseller account at [OXXA](https://www.oxxa.com)
2. Get your API credentials from OXXA dashboard
3. In HelloHost: **Settings > Domain Registrars**
4. Click **Add Registrar**
5. Select OXXA and enter credentials
6. Test connection

Now you can:
* Register domains directly from HelloHost
* Manage DNS zones
* Handle domain transfers
* Auto-renew domains

### Using Versio

Similar process for Versio with limited functionality (domain listing and auto-renewal only).

## Connecting Hosting Servers (Optional)

To automate hosting account creation:

### Using cPanel

1. Ensure you have WHM access
2. Generate an API token in WHM
3. In HelloHost: **Settings > Hosting Servers**
4. Add your server with hostname and API token
5. Test connection

### Using DirectAdmin

Similar process with DirectAdmin admin credentials.

Now when you create hosting subscriptions, HelloHost can automatically create the hosting accounts!

## Inviting Team Members

1. Navigate to **Settings > Users**
2. Click **Add User**
3. Enter their email and name
4. Assign a role:
   * **Admin** - Full access
   * **Employee** - Limited access based on permissions
5. Configure specific permissions:
   * Can view/edit clients
   * Can manage invoices
   * Can process payments
   * Can manage tasks
6. Send invitation

They'll receive an email to set up their account.

## Customizing Client Notifications

Control which emails clients receive:

**Settings > Notifications:**

* **New Invoice** - When invoices are created
* **Invoice Reminder** - For overdue invoices
* **Payment Confirmation** - After successful payment
* **Order Updates** - Order status changes
* **Renewal Reminders** - Before subscription renewals
* **Task Updates** - For public tasks

Customize timing and frequency to match your preferences.

## Using Labels to Organize Clients

Keep clients organized with labels:

1. Navigate to **Clients > Labels**
2. Create labels like:
   * "VIP Customer"
   * "Payment Issues"
   * "Monthly Plan"
   * "Yearly Plan"
3. Assign colors to labels
4. Tag clients with labels
5. Filter clients by label

## Tips for Success

### Start Simple
* Add a few clients first
* Create 2-3 basic services
* Get comfortable with the interface
* Expand from there

### Automate When Ready
* Connect payment processing to reduce manual work
* Use auto-renewal for subscriptions
* Set up recurring tasks for regular maintenance
* Connect domain registrars and hosting servers

### Keep Clients Informed
* Enable appropriate notifications
* Add clear descriptions to services
* Use the public task feature for transparency
* Send professional branded invoices

### Use the Dashboard
* Check revenue statistics regularly
* Monitor overdue invoices
* Review upcoming renewals
* Track team performance

## Common Questions

**Q: Can I import existing clients?**
A: You can manually add clients one by one, or contact support for bulk import assistance.

**Q: What if I need a service type not in the catalog?**
A: Use the "Custom Service" type - it works for any billable item.

**Q: Can clients see their subscription history?**
A: Yes! They have full access to their portal with invoices, subscriptions, and services.

**Q: How do I handle one-time payments?**
A: Create a manual invoice instead of a subscription.

**Q: Can I customize invoice templates?**
A: Branding (logo, colors) is customizable. Contact support for advanced customization.

**Q: What happens if a payment fails?**
A: The client receives a notification, and you're alerted in the dashboard.

## Getting Help

* **Documentation** - Browse the complete [Features](features.md) list
* **Configuration Guide** - See [Configuration](configuration.md) for detailed settings
* **Integrations** - Learn about [Connectors](connectors.md) for third-party services
* **Support** - Contact HelloHost support for assistance

## Next Steps

Now that you're set up:

1. **Configure domain registrars** - Automate domain operations
2. **Connect hosting servers** - Automate account provisioning
3. **Setup team permissions** - Add team members with appropriate access
4. **Customize notifications** - Control client communication
5. **Enable 2FA** - Enhance account security
6. **Explore features** - Check out the [Features](features.md) page

Welcome to HelloHost - we're excited to help grow your hosting business!
