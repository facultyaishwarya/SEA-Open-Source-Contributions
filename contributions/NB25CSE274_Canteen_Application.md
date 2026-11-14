# Online Canteen Food-Ordering System – Application Architecture Analysis

**Student Name:** Prajwal Gowda B H  
**USN:** NB25CSE274
**Case Study:** Question 2 – Mobile and Web Applications Engineering  

---

## 1. Introduction to Mobile and Web Applications

Modern digital services rely on two primary software delivery platforms:

- **Web Applications:** Software programs hosted on remote servers and accessed through standard web browsers (such as Chrome, Safari, or Edge) over the internet. Built using web technologies (HTML, CSS, JavaScript), they are platform-independent and require no installation on the user's device.
- **Mobile Applications (Native/Cross-Platform):** Software specifically engineered to run on mobile operating systems like Android and iOS. Distributed through app stores, mobile apps offer high performance, offline storage, and direct access to device hardware such as push notification services, cameras, and biometric authentication.
- **Progressive Web Applications (PWAs):** A hybrid engineering approach that uses modern browser APIs and service workers to deliver an app-like experience—including home-screen installation, offline caching, and push notifications—directly through a web URL.

---

## 2. Comparison of Mobile, Web, and PWA Approaches

| Feature / Criteria | Native Mobile Application | Traditional Web Application | Progressive Web Application (PWA) |
| :--- | :--- | :--- | :--- |
| **Installation & Access** | Must be downloaded and installed via App Store / Play Store. | Instant access via URL in any web browser; no installation. | Instant browser access with optional one-tap "Add to Home Screen." |
| **Platform Compatibility** | Separate builds or frameworks needed for Android and iOS. | Cross-platform; runs on any device with a browser. | Cross-platform; single codebase runs on Android, iOS, and desktops. |
| **Push Notifications** | Full native support for real-time order alerts. | Limited or unavailable when the browser tab is closed. | Supported via Web Push API and background Service Workers. |
| **Offline Capability** | High; stores local data and assets on device storage. | None; requires continuous internet connectivity. | Moderate to high; caches menus and static assets for weak networks. |
| **Development & Maintenance Cost** | High (store publishing fees, OS updates, dual-platform testing). | Low (single codebase, instant server-side updates). | Low to moderate (single codebase, instant updates without app store review). |

---

## 3. Selection of a Suitable Application Type with Justification

### **Selected Approach: Progressive Web Application (PWA)**

A **Progressive Web Application (PWA)** is the most suitable architecture for a college canteen food-ordering system for the following reasons:

1. **Zero Installation Friction:** Students can scan a QR code placed on canteen tables or click a campus link to browse and order immediately without downloading a dedicated app or consuming phone storage.
2. **Real-Time Order Ready Notifications:** Unlike a traditional website, a PWA utilizes Service Workers and the Web Push API to send lock-screen notifications when a student's meal is ready for pickup.
3. **Resilience in Low-Connectivity Zones:** College canteens often experience weak cellular reception or congested Wi-Fi. A PWA caches the daily menu locally so students can browse items smoothly even during brief network drops.
4. **Cost-Effective & Cross-Platform:** A single unified codebase works across Android phones, iPhones, and student laptops, eliminating Play Store/App Store approval delays and reducing maintenance costs for the college.

---

## 4. Four Major Functionalities

1. **Digital Menu Browsing & Live Availability**
   - Displays categorized food items (breakfast, lunch, snacks, beverages) with pricing, estimated preparation time, and real-time stock indicators (*Available* / *Sold Out*).
2. **Cart Management & Scheduled Order Placement**
   - Enables students to customize quantities, add special preparation notes, select immediate or break-time pickup slots, and receive a unique digital order token.
3. **Integrated Cashless Payment Processing**
   - Supports instant digital payments via UPI, debit/credit cards, net banking, and campus wallets, generating an automated digital receipt upon confirmation.
4. **Live Order Tracking & Push Notifications**
   - Updates order stages in real time (`Order Confirmed` -> `Preparing` -> `Ready for Pickup`) and triggers an automated push notification so students only visit the counter when their food is ready.

---

## 5. Three Development Challenges

1. **Peak-Hour Traffic & Concurrency Control**
   - **Challenge:** Hundreds of students place orders simultaneously during fixed 15-to-30-minute break windows, risking server slowdowns or overselling limited food quantities.
   - **Mitigation:** Implement database row-level locking for inventory counts and use lightweight caching for menu reads.
2. **Payment Synchronization Under Unstable Campus Networks**
   - **Challenge:** Network fluctuations inside canteen buildings can interrupt payment callbacks, causing scenarios where money is debited but the order is not registered.
   - **Mitigation:** Use idempotent payment APIs, webhook verification, and automated payment status reconciliation before confirming or refunding orders.
3. **Cross-Browser Push Notification Constraints (iOS vs. Android)**
   - **Challenge:** While Android browsers support web push notifications seamlessly, iOS Safari requires users to add the PWA to their Home Screen before granting notification permissions.
   - **Mitigation:** Provide a clear, guided prompt on iOS devices instructing students to tap *"Share -> Add to Home Screen"* along with SMS/email fallback alerts.

---

## 6. Simple Application Workflow Diagram

```text
+-----------------------+
|   Student Opens PWA   |
| (URL / Canteen QR)    |
+-----------+-----------+
            |
            v
+-----------------------+
| Browse Menu & Select  |
|   Food Items (Cart)   |
+-----------+-----------+
            |
            v
+-----------------------+
|  Complete Payment     |
| (UPI / Card / Wallet) |
+-----------+-----------+
            |
            v
+-----------------------+      +---------------------------+
| Order Sent to Canteen | ---> | Kitchen Dashboard Updates |
|  Kitchen Dashboard    |      | Status: "Preparing"       |
+-----------------------+      +-------------+-------------+
                                             |
                                             v
+-----------------------+      +---------------------------+
| Student Picks Up Food | <--- | Kitchen Marks "Ready" &   |
| Using Digital Token   |      | Sends Push Notification   |
+-----------------------+      +---------------------------+
