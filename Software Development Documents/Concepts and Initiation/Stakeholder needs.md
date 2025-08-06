---
title: "Stakeholder Needs"
status: "Approved"
version: "0.1"
author: "mrjclark"
date_created: "2025-08-06"
last_updated: "2025-08-06"
external_linked_controls:
  nist:
    - "SP 800-161 Ver 1:SN-1"
    - "SP 800-161 Ver 1:SN-2"
  cis:
    - "[Control Section]"
  owasp:
    - "[Document Name]:[Section]"
related_documents:
  - "[02 Software Development Charter](/FinApp/Policies/02\ Software\ Development\ Charter.md)"
contributor_roles:
  - "Project Lead"
  - "Developer lead"
  - "Security Auditor"
---
# Stakeholder needs

## Research
There are many existing personal finance and budgeting apps. Likely starting back in 2007, Mint may have been among the first to off users a system to track expenses, manage budgets and set goals. Today, there are likely hundreds available over the various platforms. 

Below is a list of the top 5 personal budget apps from the Google Play store. This will identify their key features and also look into any issues that users report with the software. This list was generated on Wednesday, August 6th, 2025.

| App Name     | Top Features                                                                 | Common Issues & Critiques                                                                 | Google Play Link |
|--------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|------------------|
| **AndroMoney** | - Multi-account support<br>- Currency conversion<br>- Excel export<br>- Graphical analytics | - Outdated UI<br>- Occasional crashes<br>- No cloud sync for free users | [AndroMoney](https://play.google.com/store/apps/details?id=com.kpmoney.android&hl=en-US) |
| **Wallet**     | - Bank sync<br>- Budget goals & bill tracking<br>- Multi-user support<br>- Real-time updates | - Sync failures<br>- App freezes<br>- Confusing UI for new users | [Wallet](https://play.google.com/store/apps/details?id=com.google.android.apps.walletnfcrel&hl=en-IN) |
| **Goodbudget** | - Envelope budgeting<br>- Manual transaction entry<br>- Sync across devices<br>- Debt tracking | - No bank sync in free version<br>- UI quirks<br>- Limited automation | [Goodbudget](https://play.google.com/store/apps/details?id=com.dayspringtech.envelopes&hl=en-US) |
| **YNAB**        | - Zero-based budgeting<br>- Goal tracking<br>- Real-time sync<br>- Educational resources | - Sluggish mobile performance<br>- Frequent UI changes<br>- High subscription cost | [YNAB](https://play.google.com/store/apps/details?id=com.youneedabudget.evergreen.app&hl=en-US) |
| **Spendee**     | - Shared wallets<br>- Custom categories & tags<br>- Visual dashboards<br>- Multi-currency support | - Bank sync failures<br>- Currency change bugs<br>- Poor customer support | [Spendee](https://play.google.com/store/apps/details?id=com.cleevio.spendee&hl=en-US) |.

Here’s a synthesized overview of the common features, frequent issues, and security concerns across the top personal finance apps on Android:


Most leading apps share these core capabilities:
- Expense Tracking: Automatic or manual logging of transactions
- Budget Creation: Zero-based, envelope, or percentage-based systems
- Bank Sync: Secure connection to financial institutions for real-time updates
- Visual Dashboards: Charts, graphs, and summaries of spending and savings
- Goal Setting: Savings targets, debt payoff plans, and financial milestones
- Multi-Device Sync: Access across phones, tablets, and desktops
- Custom Categories: Personalized tags and spending buckets
- Reminders & Notifications: Alerts for bills, budgets, and unusual activity
*Source: Number Analytics*

Despite their utility, users frequently cite these frustrations:
- Bank Sync Failures: Inconsistent or broken connections with financial institutions
- UI Complexity: Steep learning curves, cluttered interfaces, or poor onboarding
- App Crashes & Bugs: Freezing, data loss, or slow performance after updates
- Limited Customization: Rigid categories or inflexible budget structures
- Pushy Notifications: Overwhelming or poorly timed alerts
- Manual Entry Burden: Tedious transaction logging in non-automated apps
- Poor Support: Slow or unhelpful customer service responses
*Source: Responsible Budget*

Security is a growing concern, especially as apps handle sensitive financial data:
- Data Sharing with Third Parties: Nearly 75% of apps share user data (names, emails, device IDs, etc.) with external entities
- Vulnerabilities in Mobile Finance Apps: 77% of banking apps have at least one security flaw that could expose personal data
- Broad Permissions: Apps may request access to contacts, location, photos, and more—often beyond what's necessary
- Lack of Encryption Transparency: Not all apps clearly disclose their encryption or data handling practices
- Identity Theft Risk: If compromised, apps can expose users to fraud or reputational harm
*Source: USA Today*

## Conclusion
Based on this, we can see that there are some opportunities for FinApp to make a meaningful impact in the way that people do personal financing and budgeting. Due to the focus on confidentiality and integrity, we will need to ensure that data will first and always be protected from compromise, sharing, and convoluted encryption. 

## List of Stakeholder Needs

### Functional Needs
- Ability to input expenses
    - This should also allow users to customize categories, update structure and make it easy to understand
    - It should also have templates to speed up tedious tasks for entry
    - The input type can be either a single entry, or import file. If technically and securely feasible, linking to a bank should be available.
- Ability to set budgets
    - Allow users to choose the budget type, set goals, and set different categories for these
- Craft notifications based on certain triggers
    - All notifications should be configurable on when to send, what the content is, and how it is received
- The ability to automate tasks should be available
    - Automations can be time or event triggered
    - Automations can create reports, send reports, recycle permission keys
- The ability to export data for reporting, transfer, or backup should be available
    - There is an inherent risk. An option to encrypt the data should be given.
- The ability to share expenses, budgets and reports with trusted members
    - Security will be the most important part so ensuring identity will be requried.

### Non-Functional Needs
- App crashes need to be minimized
    - Crash dumps should be sent to developers to help resolve issues
- Support needs to be available and helpful
    - While there may not be humans helping, user training, FAQ's and communication channels should be known
- Costs should be kept to a minimum
    - FinApp is in no way to be monetized for personal gain. This means any expenses must be offset by the exact amount needed.
- The UI should be intuitive with what can be click, modified, and navigated to.
- The app should given indications of when it is calculating, or processing.
    - If the app is running slow due to resource constraints, this should be made known to the user

### Security Needs
- There should be a secure by default setup
    - All data at rest, in transit and in use is encrypted
    - Data exported will be encrypted
    - No PII or PFI is shared
    - Data masking is enabled for all PII and PFI on all screens
- Least privilege security needs to be enforced throughout app
    - Highly granular calls between processes
    - Unique permissions keys for each call
- All input needs to be sanitized to ensure fuzzing techniques cannot be used to defeat encryption, or security features
- MFA will be used by all non-system accounts
- Encryption used will be documented

