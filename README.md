# NeonoteX
****App Latest version:**** v1.1.2

**Developer:** KevinDGreat  
🌐 Official Website: https://neonotez.github.io

🌐 Official App site: https://neonotex.github.io

---

# What's New in NeonoteX

I am excited to announce the latest update for **NeonoteX**! This release brings new features, bug fixes, and UI improvements to enhance your experience.

## ✨ New Features

### 1. Collection Mode
- Efficiently manage client accounts and balances.
- Track monthly quotas and payments.
- Filter accounts by activity (3NM, 6NM, 9NM, 12NM, Moving, Total).
- Copy account data or view total balances with a single click.

### 2. Notepad
- Built-in notepad to store notes, reminders, or important information.
- Add, edit, and delete notes with autosave functionality.
- Easily navigate between notes using the sidebar.
- Supports large content with character limits for titles and notes.

## 🛠 Bug Fixes & Improvements
- Fixed various UI glitches for a smoother experience.
- Enhanced responsiveness across devices.
- Optimized app performance for faster loading and navigation.

---

Thank you for using **NeonoteX**! Stay tuned for more updates and features in upcoming releases.


### NeonoteX 
is an open-source offline note-taking app designed for efficient task management. Originally built for debt collectors, it allows users to create customized notes, schedule tasks, and track commitments with ease.

For debt collectors, NeonoteX helps record and monitor promises and schedule follow-ups with just a few taps. Beyond debt collection, the app can be used for a wide range of task-management needs, making it a flexible and powerful productivity tool.

---

## Features

NeonoteX offers a wide range of features that go beyond simple promise tracking:

### Promise Management
- **Add, edit, and delete promises** associated with clients or tasks.
- **Mark promises as done** with a single click.
- **Overdue detection:** Automatically marks promises past their due date as done.
- **Limit done promises:** Keeps a maximum of 50 completed promises for easier management.

### Client & Account Management
- **Create multiple accounts** to organize clients or projects.
- **Add clients** to specific accounts with descriptions and details.
- **Search clients and promises** quickly using the search bar.
- **Delete clients or accounts** with confirmation prompts to avoid accidental data loss.

### Backup & Restore
- **Export backups** of all promises and accounts with AES-256 encryption.
- **Password-protected backups** for secure storage.
- **Import backups** safely to restore previous data.

### User Interface & Experience
- **Tabbed navigation:** Quickly switch between Today, All, Done, and account-specific views.
- **Expandable promise cards:** Click on a promise or client to view more details.
- **Floating buttons:** Hide or show action buttons for a cleaner interface.
- **Offline-first experience:** All data is stored locally, making the app usable without an internet connection.
- **Installable PWA:** Install NeonoteX on your device for an app-like experience.

### Notifications & Prompts
- **Custom notifications** for actions like successful backup restoration.
- **Confirmation modals** to prevent accidental deletion of promises, clients, or accounts.

### Advanced Features
- **Search auto-clear:** Automatically clears search results after 10 seconds of inactivity.
- **Move promises:** Edit or move promises to different dates or clients.
- **Secure cryptography:** Uses Web Crypto API for password-protected backups.
- **Service Worker Support:** Works as a Progressive Web App (PWA) with offline capabilities.

---

# NeonoteX Features – Collection & Notepad

## Collection Management

NeonoteX includes a robust **Collection** module to manage account balances, track payments, and monitor monthly quotas. This module is ideal for businesses or teams that need to track multiple client accounts and ensure timely collections.

### Accessing Collection Module
- Open the Collection panel by clicking the **Collection** button (`collectionBtn`) in the main interface.
- Close the panel using the **Close** button (`closeCollectionModal`).

### Tabs & Categories
Collection records are organized into several tabs based on account activity duration:
- **3NM**: 3 Months Non-moving Accounts
- **6NM**: 6 Months Non-moving Accounts
- **9NM**: 9 Months Non-moving Accounts
- **12NM**: 12 Months Non-moving Accounts
- **Moving**: Accounts with active movement
- **Total**: All accounts combined  

Each tab dynamically filters the displayed accounts according to the category.

### Adding & Updating Collection Records
- **Add New Record**: Enter client **Name**, **Balance**, **Last Paid Date**, and optional **Payment**.  
- **Update Record**: Edit the same fields to update an existing client record.  
- **Automatic Balance Adjustment**: When adding a payment, the balance is automatically reduced, and monthly running totals are updated.
- **Persistent Storage**: All collection data is stored in `localStorage` (`collectionData` and `collectionQuotaData`).

### Quota & Monthly Tracking
- **Set Monthly Quota**: Enter the target quota for a selected month.
- **Track Running Total**: Displays total payments made vs. quota.
- **Percentage Completion**: Dynamically updates to show the progress toward the monthly quota.
- **Monthly Account Counts**: Automatically tracks the number of accounts recorded per month.

### Searching & Filtering
- Use the **Search** input (`collectionSearch`) to filter collection records by client name.
- Tabs automatically adjust to display only accounts that match the selected category.

### Copy & Balance Tools
- **Copy Collection**: Copies all visible accounts in the selected tab to clipboard in a structured format.
- **Balance of Button**: Shows the total receivable balance for the currently selected tab with a notification popup.

### UI Features
- **Expandable Panel**: Toggle detailed info using the **Expand Panel** button.
- **Dynamic Account List**: Clicking a client name auto-fills their data for updates.
- **Delete Records**: Each record can be deleted individually with confirmation.

### Data Keys
- `collectionData`: Array of all collection records  
- `collectionQuotaData`: Object storing monthly quotas and balances  
- `monthlyAccountCounts`: Tracks total accounts added per month  

---

## Notepad Feature

NeonoteX provides a built-in **Notepad** to store notes related to your accounts, projects, or personal tasks.

### Accessing Notepad
- Open the Notepad panel using the **Notepad** button (`notepadBtn`).
- Close the panel using the **Close** button (`closeNotepad`).

### Notes Management
- **Add Note**: Click **Add Note** (`addNoteBtn`) to create a new note with empty title and content.
- **Select Note**: Click a note in the sidebar list to load it into the editor.
- **Delete Note**: Delete a note using the ❌ button next to it. Confirmation is required.
- **Edit Note**: Directly edit the **Title** (`noteTitle`) and **Content** (`noteContent`), with live autosave to `localStorage`.
- **Character Limit**:
  - Title: 100 characters  
  - Content: 20,000 characters  

### Sidebar Features
- **Toggle Sidebar**: Collapse or expand the note list using the **Toggle Notes** button (`toggleNotes`).
- **Real-time Update**: Notes list updates automatically whenever a note is added, updated, or deleted.

### Data Storage
- Notes are stored in `localStorage` under the key `neonote_notes`.  
- Each note object contains:
  ```json
  {
    "id": "note_123456789",
    "title": "Note Title",
    "content": "Note content text..."
  }
  

---

## Use Cases

NeonoteX is designed for debt collectors, Managers, and small businesses, but its flexible features make it useful in many scenarios:

- Tracking client promises and other tasks.
- Organizing project tasks and deadlines.
- Managing multiple client accounts and contacts.
- Keeping detailed notes for follow-ups or appointments.
- Securely backing up and restoring sensitive data.
- Using offline in areas with limited or no internet connectivity.

