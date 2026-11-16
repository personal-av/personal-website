# Secure Dashboard - Encrypted Data Management System

A secure, client-side encrypted dashboard for managing sensitive data. No server required, all data is encrypted on your computer using AES-256-GCM encryption.

## Features

- **🔒 Military-grade Encryption**: AES-256-GCM with PBKDF2 key derivation (100,000 iterations)
- **💾 File-based Storage**: Your data stays on YOUR computer in an encrypted `data.js` file
- **🌍 Multi-Device Access**: Access your data on unlimited devices via cloud sync, USB, or manual transfer
- **🌐 Cross-browser Compatible**: Works in Chrome, Edge, Firefox, and Safari
- **⏱️ Auto-lock**: Automatically locks after 5 minutes of inactivity
- **📋 Click-to-copy**: Copy any cell value to clipboard with a single click
- **🚫 No Server Required**: Runs entirely in your browser - just open the HTML files
- **🔄 Hybrid File Access**: Smart file handling adapts to your browser
- **☁️ Cloud Storage Ready**: Safe to store in Google Drive, Dropbox, OneDrive (file is encrypted)

## What's Included

- **admin.html** - Full-featured admin interface for creating and editing data
- **dashboard.html** - Password-protected viewer with auto-lock security
- **README.md** - This file with complete instructions

## Quick Start

### 1. Download the Files

Download these three files to your computer:
- `admin.html`
- `dashboard.html`
- `README.md`

### 2. Create Your Dashboard

1. **Open admin.html** in your browser (double-click the file)
2. **Click "Create New Dashboard"**
3. **Set a strong password** (you'll need this to access your data)
4. **Choose where to save your data.js file** (recommended: Documents folder or USB drive)

### 3. Add Your Data

1. **Create tabs** for different categories (e.g., "Passwords", "Bank Accounts", "API Keys")
2. **Add columns** for each field you need (e.g., "Website", "Username", "Password")
3. **Add rows** with your data
4. **Click Save** to encrypt and save your data

### 4. View Your Dashboard

1. **Open dashboard.html** in your browser
2. **Select your data.js file** (only needed once in Chrome/Edge)
3. **Enter your password**
4. **View your data** securely with auto-lock protection

## Browser-Specific Instructions

### Chrome & Edge Users (Recommended)

**Best Experience** - File handle is remembered!

#### First Time Setup:
1. Open `admin.html`
2. Click "Create New Dashboard"
3. Choose where to save `data.js` (e.g., Documents folder)
4. Your browser will remember this location

#### Subsequent Uses:
1. Open `admin.html` - it will automatically load your data
2. Enter your password
3. That's it! No need to re-select the file

**Saving Data:**
- Click "Save" and your data.js file is updated instantly
- No downloads, no manual file management

**Important:** If you close your browser completely, you may need to grant permission again when you reopen.

### Firefox & Safari Users

**Manual File Selection** - Browser limitation requires selecting file each time

#### Every Time You Use It:
1. Open `admin.html`
2. Click "Load Existing Dashboard"
3. **Select your data.js file** (you'll need to do this each time)
4. Enter your password

**Saving Data:**
- Click "Save"
- A new `data.js` file will download
- **Replace your old data.js file** with the downloaded one
- Keep your data.js file in a consistent location (e.g., Documents folder)

**Tip:** Keep your data.js file in an easy-to-find location so selecting it each time is quick.

## Security Features

### Encryption Details
- **Algorithm**: AES-256-GCM (military-grade encryption)
- **Key Derivation**: PBKDF2-SHA256 with 100,000 iterations
- **Salt**: Random 16-byte salt (unique per encryption)
- **IV**: Random 12-byte initialization vector (unique per encryption)

### What This Means
- ✅ Your data is encrypted at rest (on disk)
- ✅ Only decrypted in memory while you're using it
- ✅ Password never stored anywhere
- ✅ Even if someone steals your data.js file, they can't read it without your password

### Auto-Lock Feature
- Dashboard automatically locks after **5 minutes** of inactivity
- Timer resets when you interact with the page
- Countdown displayed in header
- All sensitive data cleared from memory on lock

### Password Protection
- Strong encryption requires a strong password
- Use a unique password you don't use elsewhere
- Recommended: 12+ characters with mix of letters, numbers, symbols
- **Important**: If you forget your password, your data cannot be recovered

## Column Types

The system supports three column types:

### 1. Text (Default)
- Regular text display
- Good for: Names, descriptions, notes

### 2. Password
- Displayed as plain text (for easy copying and viewing)
- Auto-detected for columns named: password, pass, pwd, secret, key, token, auth
- Good for: Passwords, API keys, secret tokens

### 3. URL
- Displayed as clickable links
- Opens in new tab
- Auto-detected for URLs starting with http:// or https://
- Good for: Website links, documentation URLs

## File Management

### Where to Store data.js

**Recommended Locations:**
- 📁 Documents/SecureDashboard/data.js
- 📁 Desktop/data.js
- 💾 USB Drive (for portability)
- ☁️ Encrypted cloud storage (Dropbox, Google Drive, etc.)

**Security Tips:**
- Keep backups in multiple locations
- Consider storing on an encrypted USB drive
- Cloud storage is safe (file is already encrypted)
- Never email your data.js file

### Backup Strategy

**Important:** Always keep backups!

1. **Copy your data.js file** to multiple locations
2. Consider versioning: `data-2025-12-29.js`
3. Test your backups occasionally
4. Store backups in different physical locations

### Multi-Device Access - Access Your Data Anywhere

Your encrypted data.js file is **100% portable** and can be accessed on unlimited devices without recreating data!

#### Quick Setup for Multi-Device Access

**One-Time Setup on Each Device:**

1. **Download the HTML files** on each device:
   - Download `admin.html` and `dashboard.html`
   - Save to an easy-to-find location (e.g., Desktop, Documents)

2. **Put data.js in cloud storage** (recommended) OR use USB/manual transfer

**That's it!** Now you can access your data on any device.

---

#### Method 1: Cloud Storage (Recommended) ⭐

**Why this works:** Your data.js file is already encrypted, so cloud storage is safe!

**Setup:**

1. **Choose a cloud service:**
   - ✅ Google Drive
   - ✅ Dropbox
   - ✅ OneDrive
   - ✅ iCloud Drive
   - ✅ Any sync service

2. **Place data.js in synced folder:**
   ```
   Example:
   Google Drive/SecureDashboard/data.js
   Dropbox/SecureDashboard/data.js
   OneDrive/SecureDashboard/data.js
   ```

3. **On each device:**
   - Wait for sync to complete
   - Open `admin.html` or `dashboard.html`
   - Select the synced `data.js` file
   - Enter your password

**Benefits:**
- ✅ Automatic sync across all devices
- ✅ Always access latest data
- ✅ Safe (file is encrypted)
- ✅ Built-in backup
- ✅ No manual copying needed

**Chrome/Edge Bonus:**
- Select the cloud-synced `data.js` once
- Browser remembers the location
- Auto-loads on subsequent opens
- Changes sync automatically

---

#### Method 2: USB Drive (Portable)

**Perfect for:** No internet, maximum privacy, offline access

**Setup:**

1. **Copy to USB drive:**
   ```
   USB Drive/
   ├── admin.html
   ├── dashboard.html
   └── data.js
   ```

2. **Use on any computer:**
   - Plug in USB drive
   - Open `admin.html` or `dashboard.html` from USB
   - Select `data.js` from USB
   - Enter password

**Benefits:**
- ✅ Works offline
- ✅ No cloud dependency
- ✅ Physical control
- ✅ Portable workstation

---

#### Method 3: Manual Transfer

**For occasional multi-device access**

**Transfer data.js using:**
- 📧 Email to yourself (safe - file is encrypted)
- 💬 Messaging apps (Telegram, WhatsApp, Signal)
- 🔗 File transfer services (WeTransfer, Send Anywhere)
- 📱 AirDrop (Mac/iOS)
- 🔵 Bluetooth transfer

**Steps:**
1. Transfer `data.js` from Device A to Device B
2. On Device B, open `admin.html` or `dashboard.html`
3. Select the transferred `data.js`
4. Enter password

---

#### Multi-Device Workflow Examples

**Example 1: Home + Work Computer (Cloud Sync)**

```
Setup:
- Put data.js in Google Drive/MyDashboard/
- Install admin.html and dashboard.html on both computers
- Point both to the Google Drive data.js

Usage:
1. Edit data at work → Saves to Google Drive
2. Google Drive syncs in background
3. Open at home → Latest data available
4. Make changes at home → Syncs back
```

**Example 2: Desktop + Laptop + Phone (Cloud + Browser)**

```
Setup:
- data.js in Dropbox
- admin.html on desktop for editing
- dashboard.html on laptop and phone for viewing

Usage:
- Desktop: Edit and manage data
- Laptop: View data in meetings
- Phone: Quick reference on the go
- All sync via Dropbox
```

**Example 3: Multiple Devices + USB Backup**

```
Setup:
- Primary: data.js in OneDrive (synced)
- Backup: Copy to USB weekly

Usage:
- Day-to-day: Access via OneDrive on all devices
- Offline travel: Use USB copy
- After travel: Sync USB back to OneDrive
```

---

#### Important Multi-Device Notes

**Handling Conflicts:**

⚠️ **If editing on multiple devices simultaneously:**

1. **Last save wins** - newer file overwrites older
2. **Best practice:** Only edit on one device at a time
3. **If conflict occurs:**
   - You'll have two versions of data.js
   - Choose the most recent one
   - Manually merge if needed

**Cloud Sync Timing:**

- Wait 10-30 seconds for sync to complete
- Check sync status before switching devices
- Look for "✓ Synced" indicator in cloud app

**Browser Memory (Chrome/Edge):**

- Each device remembers its own file location
- Changing cloud folder? Update on each device
- Click "Change File" button to reselect

**Password Consistency:**

- ⚠️ **Use same password on all devices** (obviously!)
- Changing password? Must update everywhere
- New password encrypts new saves

---

#### Security Best Practices for Multi-Device

✅ **Safe practices:**
- Use cloud storage (file is encrypted)
- Email to yourself (file is encrypted)
- Share via messaging apps (file is encrypted)
- Store on public cloud (file is encrypted)

⚠️ **Remember:**
- File is safe even if intercepted
- Password is the only key
- No password = no access
- Keep password separate from file

❌ **Don't:**
- Store password in same cloud folder
- Email password with file
- Share password via insecure channels
- Write password in file name

---

#### Quick Reference: Device Setup Checklist

**On each new device:**

- [ ] Download `admin.html` (for editing)
- [ ] Download `dashboard.html` (for viewing)
- [ ] Install on Desktop or Documents folder
- [ ] Set up access to data.js (cloud/USB/transfer)
- [ ] Test: Open admin.html, select data.js, enter password
- [ ] Test: Open dashboard.html, select data.js, enter password
- [ ] Bookmark or create desktop shortcut for easy access

**First time on new device:**
- Browser may ask to select file (normal)
- Chrome/Edge: Will remember after first selection
- Firefox/Safari: Must select each time (browser limitation)

---

Your data is now accessible everywhere! 🌍

## Usage Tips

### Admin Panel (admin.html)

**Managing Tabs:**
- Click **[+]** next to "Tabs" to create a new tab
- Click a tab name to view/edit its contents
- Click **Rename** to change tab name
- Click **Delete Tab** to remove (with confirmation)

**Managing Columns:**
- Click **Add Column** to add a new field
- Choose column type (Text, Password, URL)
- Click **[×]** next to column name to delete
- Columns apply to all rows in the tab

**Managing Rows:**
- Click **Add Row** to insert new data
- Click **Edit** to modify existing row
- Click **Delete** to remove row
- All changes saved when you click **Save**

**Keyboard Shortcuts:**
- `Ctrl/Cmd + S` - Save (prompts to save before closing)

### Dashboard (dashboard.html)

**Viewing Data:**
- Click tabs to switch between categories
- Click any cell to copy value to clipboard
- All data displayed as plain text for easy viewing

**Security:**
- Auto-locks after 5 minutes of inactivity
- Timer shown in header
- Moving mouse or typing resets timer
- Click **🔒 Logout** to manually lock

## Troubleshooting

### "Wrong password" error
- Double-check your password (case-sensitive)
- Try typing slowly to avoid errors
- Make sure Caps Lock is off

### "No data file selected" error
- You cancelled the file picker
- Try again and select your data.js file
- Make sure you're selecting the correct file

### File handle lost (Chrome/Edge)
- Browser cache was cleared
- Browser was completely restarted
- Solution: Just select your data.js file again - it will be remembered

### Downloaded file isn't saving (Firefox/Safari)
- Check your Downloads folder
- Manually move the new data.js to replace your old one
- Make sure you're not just opening it from Downloads

### "Decryption failed" error
- File may be corrupted
- Restore from backup
- Make sure you're using the correct data.js file

### Auto-lock not working
- Make sure JavaScript is enabled
- Try refreshing the page
- Check browser console for errors (F12)

## Technical Details

### System Requirements
- Modern web browser (2020+)
- JavaScript enabled
- Web Crypto API support (all modern browsers have this)

### Browser Compatibility

| Browser | Version | File System Access | Manual Fallback |
|---------|---------|-------------------|-----------------|
| Chrome  | 86+     | ✅ Yes            | ✅ Yes          |
| Edge    | 86+     | ✅ Yes            | ✅ Yes          |
| Firefox | 90+     | ❌ No             | ✅ Yes          |
| Safari  | 14+     | ❌ No             | ✅ Yes          |

### Data Format

Your data.js file contains:
```javascript
window.ENCRYPTED_DATA = "base64_encrypted_string";
```

**Structure:**
- Base64-encoded encrypted data
- Contains: salt (16 bytes) + IV (12 bytes) + encrypted content
- Encrypted content: JSON with tabs, columns, rows

### Security Considerations

**Protected Against:**
- ✅ File theft (encrypted at rest)
- ✅ Memory dumps after logout (data cleared)
- ✅ Session hijacking (auto-lock)
- ✅ Unauthorized access (password-protected)

**NOT Protected Against:**
- ❌ Shoulder surfing while unlocked (data displayed as plain text)
- ❌ Browser dev tools while unlocked (close when not in use)
- ❌ Keyloggers on your computer (use secure device)
- ❌ Browser extensions with page access (review extensions)
- ❌ Compromised operating system (keep OS updated)

## FAQ

### Q: Is my data sent to any server?
**A:** No! Everything runs in your browser. Your data never leaves your computer except when YOU copy it somewhere.

### Q: Can I use this on multiple computers?
**A:** Yes! Your data.js file is 100% portable. See the **"Multi-Device Access"** section above for detailed instructions on using cloud storage (recommended), USB drives, or manual transfer to access your data on unlimited devices.

### Q: What if I forget my password?
**A:** Unfortunately, there's no password recovery. If you forget your password, your data cannot be decrypted. This is by design for security.

### Q: Can someone crack my encryption?
**A:** AES-256-GCM is military-grade encryption. With a strong password (12+ characters), it would take billions of years to crack with current technology.

### Q: Why does Firefox/Safari require more steps?
**A:** Browser limitation. Chrome/Edge support the File System Access API which allows persistent file handles. Firefox/Safari don't support this API yet.

### Q: Can I sync this with cloud storage?
**A:** Absolutely! This is the **recommended approach** for multi-device access. Since your data.js is encrypted, it's completely safe in Google Drive, Dropbox, OneDrive, iCloud, or any cloud service. See the **"Multi-Device Access"** section above for detailed cloud sync setup.

### Q: How do I change my password?
**A:** In admin.html, click "Change Password" in the header. Enter your new password and click Save.

### Q: Can I export my data?
**A:** Your data.js file IS your export. Copy it anywhere. You can also open it in admin.html and manually copy the data you need.

### Q: Is this safe for storing passwords?
**A:** Yes, with caveats. It's secure from file theft and casual browsing. However, password managers like 1Password or Bitwarden have additional features like auto-fill, password generation, and breach monitoring. This tool is best for data you access less frequently or need full control over.

## Advanced Usage

### Backup Automation (Windows)

Create a batch file to backup your data.js:

```batch
@echo off
copy C:\Users\YourName\Documents\data.js C:\Users\YourName\Backups\data-%date:~-4,4%-%date:~-10,2%-%date:~-7,2%.js
```

### Backup Automation (Mac/Linux)

Create a shell script:

```bash
#!/bin/bash
cp ~/Documents/data.js ~/Backups/data-$(date +%Y-%m-%d).js
```

### Custom Column Types

You can manually edit data.js (after decryption in admin.html) to add custom logic, but this requires programming knowledge and isn't officially supported.

## Version History

**v1.0** (2025-12-29)
- Initial release
- AES-256-GCM encryption
- Hybrid file access (File System Access API + manual fallback)
- Admin and dashboard interfaces
- Auto-lock functionality
- Click-to-copy feature
- Auto-detection of column types
- Multi-device access support

## Quick Start: Multi-Device Setup

**Want to access your data on multiple devices?** Here's the fastest way:

### Option A: Cloud Storage (Best for Most Users)

```
1. Save data.js to Google Drive/Dropbox/OneDrive
2. On each device:
   - Download admin.html & dashboard.html
   - Open either file
   - Point to your cloud-synced data.js
   - Enter password
3. Done! Changes sync automatically
```

### Option B: USB Drive (For Offline/Privacy)

```
1. Copy everything to USB:
   - admin.html
   - dashboard.html
   - data.js
2. Plug USB into any computer
3. Open files from USB
4. All data portable!
```

### Option C: Manual Transfer

```
1. Email data.js to yourself (safe - it's encrypted!)
2. Download on other device
3. Open admin/dashboard and select data.js
4. Enter password
```

**📖 See "Multi-Device Access" section above for detailed instructions**

---

## License

This software is provided as-is, without warranty of any kind. Use at your own risk.

## Support

For issues, questions, or contributions:
- Check the Troubleshooting section above
- Review the FAQ
- Open an issue on GitHub (if applicable)

## Security Disclosure

If you discover a security vulnerability, please email it privately rather than posting publicly.

---

**Remember:** Always keep backups, use a strong password, and never share your password with anyone!

Enjoy your secure dashboard! 🔒
