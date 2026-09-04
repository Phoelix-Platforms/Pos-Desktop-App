# Phoelix POS — Setup Guide

Welcome to Phoelix POS. This guide walks you through installing the app, setting
up your shop, and getting your first sale on the receipt. No technical knowledge
needed — just follow the steps in order.

---

## 1. What you're setting up

Phoelix POS runs your shop's sales, products, staff, and reports. It works on one
computer or several:

- **Main Till** — the primary computer that stores all your data. Every shop has
  **exactly one** Main Till.
- **Connected computers** — extra tills or an office PC that connect to the Main
  Till over your shop's WiFi/network and share the same data.

If you only have one computer, it is the Main Till. That's perfectly fine.

---

## 2. Before you start

- A Windows 10 or Windows 11 computer (64-bit).
- The **Phoelix POS Setup** installer file you downloaded.
- A receipt printer (optional, but recommended) already plugged in and installed
  in Windows.
- If you'll use more than one computer, make sure they're all on the **same WiFi
  or network**.

---

## 3. Install the app

1. Double-click **`Phoelix_POS_Setup.exe`**.
2. If Windows shows a blue **"Windows protected your PC"** box, click
   **More info → Run anyway**. (This just means the app isn't yet code-signed —
   it's safe.)
3. Choose where to install (the default is fine) and finish. A **Phoelix POS**
   shortcut appears on your desktop.

---

## 4. First launch — pick your role

The first time you open Phoelix POS, it asks how this computer should run:

- On your **main shop computer**, choose **"Main Till"**. It will set up your
  database — this takes a few moments the first time. Please wait for it to finish.
- On any **extra computer**, choose **"Connect to Main Till"**. It automatically
  finds the Main Till on your network.

> **If Windows Firewall asks for permission**, click **Allow**. This is needed so
> extra computers can connect and so receipt printing works. If you miss it, allow
> "Phoelix POS" later under Windows Firewall settings.

You only pick a role **once** per computer.

---

## 5. Log in — then change the password immediately

The app comes with one built-in administrator account:

| | |
|---|---|
| **Username** | `admin` |
| **Password** | `admin123` |
| **Override PIN** | `9999` |

**Your very first task after logging in is to change this password.** Everyone
who installs Phoelix POS starts with the same one, so leaving it unchanged is not
safe for a real shop. Change the **Override PIN** too (see section 8) — it's what
lets a manager approve a cashier voiding items or clearing a sale.

1. Log in with `admin` / `admin123`.
2. Go to **Staff & Payroll**.
3. Find the **Admin** account and use **Reset Password** to set your own strong
   password.
   - *If you don't see a password option for Admin, instead create a new staff
     account with the Admin role and a strong password, and use that from now on.*

Keep your new password somewhere safe — there's no "forgot password" email.

---

## 6. Set up your shop

Work through these in the sidebar:

1. **Settings** — enter your **store name, address, and phone number**. These
   print at the top of every receipt. Set your **receipt footer note** too (e.g.
   "Thank you for your patronage!").
2. **Products** — add your product categories and products (name, price, stock).
3. **Staff & Payroll** — add a login for each cashier so sales are tracked per
   person. Give cashiers the Cashier role, not Admin.

---

## 7. Set up your receipt printer

1. Make sure your thermal printer is installed in Windows and prints a Windows
   test page.
2. In Phoelix POS, open **Settings** and select your printer as the receipt
   printer.
3. Make a test sale from the **Cashier Terminal** and confirm the receipt prints.

Receipts automatically show each item, its quantity (e.g. `x 2`), the total number
of items, and your store details. Long product names wrap neatly and are never cut
off.

### Using more than one computer?

Each computer prints on **its own** printer. A receipt always prints on the
computer that rang up the sale, using the printer selected **on that same
computer** — the Main Till's choice does **not** carry over to a connected till.
So the printer you pick on the admin/Main Till PC only affects that PC.

To set the printer on a connected cashier PC, do **one** of these on that PC:

- **Easiest:** in Windows, set the thermal printer as that computer's **default
  printer**. Phoelix POS will use it automatically — no in-app setting needed.
- **Or:** log in as an admin on that computer, open **Settings**, and select the
  printer there. That choice is saved on that PC only.

Repeat this once for every computer that needs to print.

---

## 8. The manager override PIN (voiding & clearing carts)

Cashiers sometimes need to remove an item from a sale or clear the whole cart —
for example when a customer changes their mind. To stop this being abused, the
till asks for a **manager override PIN** before it will void a line or clear the
cart:

- A **cashier** is prompted to enter the override PIN. Only someone who knows it
  (your manager/admin) can approve the action.
- An **admin** logged in at the till is trusted automatically and isn't prompted.

The app ships with a **default override PIN of `9999`**. Change it to your own
code as soon as you're set up:

1. Go to **Staff & Payroll**.
2. Find your **Admin** account and click **Set PIN**.
3. Enter a new code of **up to 4 digits** and save. A small marker shows which
   admin accounts have a PIN set.

You can also give an override PIN to an admin when you first create them, using
the **Add Staff** form (the PIN box appears only when the role is Admin).
Cashiers never have their own override PIN — the code is a manager's key.

> **Tip:** treat the override PIN like a manager's key — share it only with people
> you trust to approve refunds and voids, and change it if it leaks.

---

## 9. Back up your data (please don't skip this)

Your sales data lives on your Main Till computer. Protect it:

- **Local / USB backup** — in **Settings**, choose a backup folder (a USB stick is
  great). This works instantly, no account needed.
- **Google Drive backup** — in **Settings**, click **Connect Google
  Drive**, sign in to your Google account, and approve access. Then use **Backup
  Now**, and daily backups run automatically.
  - The first time, Google may warn that the app is "unverified" — click
    **Advanced → Continue** to proceed. Phoelix POS can only ever see backup files
    it created, nothing else in your Drive.

**Restoring** a backup replaces your current data — but the app automatically saves
a safety copy of your current data first, just in case.

---

## 10. Free trial & subscription

- Phoelix POS starts with a **30-day free trial** from your first setup.
- You'll see reminders as the trial nears its end.
- To keep using the app after the trial, click **Subscription** (top of the screen)
  or **Renew Subscription** in the sidebar, then **Pay with Paystack**. Payment adds
  another 30 days.
- If a subscription lapses, the app locks to the payment screen until you renew —
  **your data is never deleted**, it's just paused until you pay.

---

## 11. Using more than one computer

- Keep the **Main Till on and connected** to the network whenever the shop is open.
- Connected computers share the same products, sales, and reports live.
- If a connected computer can't find the Main Till, see Troubleshooting below.

---

## 12. Troubleshooting

**A connected computer can't find the Main Till**
- Are both computers on the **same WiFi/network**?
- Is the **Main Till turned on** and Phoelix POS open?
- Was **Windows Firewall allowed** on the Main Till? Re-allow "Phoelix POS" if unsure.

**The receipt won't print**
- Is the printer on, loaded with paper, and selected in **Settings**?
- Does it print a Windows test page? If not, fix the printer in Windows first.

**"Subscription locked" message**
- Your trial or subscription has ended. Click **Subscription → Pay with Paystack**
  to restore access instantly. Your data is safe.

**The app won't start / a database error appears**
- Close any other program using Apache, or MySQL, then reopen Phoelix POS.
- Restart the computer and try again.

**Do NOT delete app data files**
- Never delete Phoelix POS files inside your AppData folder to "reset" the app —
  this can erase your shop's database. Contact us instead via our website.

---

## 13. Need help?

Contact **Phoelix Platforms Ltd** through our website. When reporting a problem, tell us what you were doing and the
exact message on screen.

*Thank you for using Phoelix POS.*
