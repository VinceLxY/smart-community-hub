# Smart Community Hub

A resident-centred service layer for the **Township of Tomorrow**.
Submission for the Sime Darby Property University Hackathon 2026.

Smart Community Hub brings everyday residential services into one platform: **Smart Locker**, **Visitor Pass**, **Lift Booking** and **Community Pulse**. A clickable prototype demonstrates every flow, with four role views (Resident, Guard, Courier, Manager) that share the same data.

- Live prototype: `[paste your GitHub Pages link here]`
- Demo video: `[paste your YouTube link here]`

## How to open the prototype

**Online:** open the live prototype link above in any modern browser (phone or desktop).

**Offline:** download `index.html` and double-click it. No installation, server or login is needed.

Notes:
- All data is stored in your own browser (localStorage). Nothing is sent to a server.
- To start again from a clean state, tap **Reset demo data** in the app, or clear this site's data in your browser.
- QR codes, lockers and lifts are **simulated**. There is no connection to physical gates, lockers or lift controllers.

## The four roles

Use the tabs at the top of the app to switch role: **Resident, Guard, Courier, Manager**. All roles share the same live data, so an action in one role appears in the others. The in-app **Demo guide** button gives a short walkthrough.

## Suggested walkthrough (about 5 minutes)

### 1. Community Pulse (Resident, then Manager)
1. As **Resident**, open **Pulse**. A corridor light issue already has 19 supporters.
2. Add your support. It reaches the threshold of 20 residents, and management now has 48 hours to respond.
3. Switch to **Manager**, open the **Community Pulse** tile (Issues), type a response and send it. Supporters are notified.
4. Back as Resident, report a new issue and tick **Urgent**. An urgent report is private: only the resident and management see it. The Manager gets a red alert with a 4-hour response time.

### 2. Smart Locker (Resident, Courier)
1. As **Resident**, open **Locker**, pick a free locker and reserve it. One six-digit code is generated. Use the copy button to copy it.
2. Switch to **Courier**. Enter a wrong code (it is rejected), then the correct code to deposit the parcel.
3. Back as Resident, the parcel is shown as deposited and the same code unlocks it for collection.
4. A reservation that is not used within 12 hours is released automatically.

### 3. Visitor Pass (Resident, Guard, Manager)
1. As **Resident**, open **Visitor**, enter the guest name, pick the date on the calendar and a time window. You can repeat the pass for several days.
2. A QR pass is created. Switch to **Guard**, use **Scan QR** (or type the pass token, e.g. `VP-AB12CD`), and check the guest in and out.
3. The **Demo** button creates a pass that expires in 1 minute, which shows the overstay flag.
4. As **Manager**, open the **Visitor Pass** tile. Management sees only who came in and out, and when.

### 4. Lift Booking (Resident, Manager)
1. As **Resident**, open **Lift**, choose a date on the calendar and a slot between 09:00 and 17:00, then send the request.
2. Switch to **Manager**, open the **Lift Booking** tile (Lifts). To **reject**, a reason is required. To **approve**, a supervisor must be assigned.
3. Back as Resident, the approved booking shows the supervisor's name and a QR code. An approved slot not used within 15 minutes is released.

### 5. Manager overview and notices
As **Manager**, the overview shows lift requests waiting, issues waiting, lockers in use, visitors inside and response times. Publish a notice and it appears at the top of the Resident home page.

## What is real and what is simulated

| Real in the prototype | Simulated |
| --- | --- |
| Workflows, statuses, rules and timers | QR scanning and validation |
| Role-based views and permissions | Locker hardware and lock detection |
| Notifications and approvals | Lift access control |

Production deployment would require server-side validation, access control and hardware integration (see the pitch deck, slides 5, 7 and 8).

## Privacy design

- Residents see support for an issue as a count, never by name.
- Urgent reports are private to the resident and management.
- Management sees visitor names and in/out times only.
- Design policy: visitor details are deleted 30 days after a pass ends.

## Technology

Single-file web app (HTML, CSS, vanilla JavaScript). The QR display uses the `qrcodejs` library. Proposed production stack: Supabase or Firebase for data and authentication.

## Team

**Team: Synapse 3**

- VINCENT LIM XUN YANG
- YEOH YEE NAN
- TEOH HOU XIANG

**University:** Universiti Utara Malaysia

**Contact:** vincentlimxy@gmail.com
