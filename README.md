# Enterprise_Quality_Spackle 🛠️

> **The Philosophy:** 4 Singles = 1 Home Run. A series of small wins will often count the same, get more people involved, and are often more sustainable than a "grand slam" project that no one will use.

---

## 🐙 Case Study:'The Kraken'
**VBA as Middleware: How a Monster Report Was Tamed**

In any large organization, there is often a natural tension between HQ technical teams and front-line managers. This is the story of **The Kraken**—an enterprise report so complex it nearly drowned the department it was meant to save.

### 🚩 The Problem: Enterprise Over-Engineering
Our HQ report writers are brilliant and hardworking, but they built a data-science marvel that was a nightmare for end-users. 

* **The Scale:** The report utilized **[multiple integrated queries](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/HQ_SQL_KRAKEN)** to pull approximately **400 table elements**
<img width="913" height="657" alt="image" src="https://github.com/user-attachments/assets/f08ebdc8-0161-4c1d-ab1b-a507eb1cb2c5" />


* **The Complexity:**
 
  - It featured **200 custom calculation variables...**
<img width="801" height="655" alt="image" src="https://github.com/user-attachments/assets/72d021c5-f03b-4aff-8efc-aac33205532b" />

---

  - many of which added substantial **dimensional complexity** within themselves
<img width="1080" height="411" alt="image" src="https://github.com/user-attachments/assets/bca63865-f004-43e6-bcf5-f15d8be2d52b" />

---

  - It featured **68 different formatting rules**
<img width="550" height="396" alt="image" src="https://github.com/user-attachments/assets/baf08218-9ff1-4593-a425-410419880413" />

---

* **The Result:** A "monster" output 
<img width="1870" height="738" alt="image" src="https://github.com/user-attachments/assets/be6d5cff-121a-43c9-b590-ccb432f97e07" />

---

* **The REAL Problem?**
* A fundamental non-understanding of a Rehab Manager's day! She's not sitting in an office with a dual-monitor workstation - she's on the floor working with kids...and a 15" laptop
<img width="1867" height="677" alt="image" src="https://github.com/user-attachments/assets/541f9170-6eae-430e-b95a-5888e18e99ec" />

* **The Human Cost:** Managing the queues became almost a full-time job for the Rehab Manager. Revenue integrity stalled whenever the manager was away.

---

### 🛠️ The Solution: The 'Spackle' Strategy
Re-engineering the HQ report would be too expensive and time-consuming. Not to mention the potential for hurt feelings. Instead, I used the tools at hand to get the data over the "last mile" to the customer.

I wrote a [**comprehensive VBA script**](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/KRAKEN_SLAYER_VBA) that transformed this monster into a manageable workflow:
1.  **Decoder Ring:** The script reads the HQ report and automatically decodes the RGB flags into plain English status updates.
   <img width="780" height="227" alt="image" src="https://github.com/user-attachments/assets/d2471a24-3ac9-424c-b9ee-c39f2c53772b" />

2.  **Automated Distribution:** Instead of one person manually sorting rows, the script parses the data and distributes individual queues to the **20+ therapists** via Outlook.
3.  **Revenue Integrity Master DB:** The script maintains a master database to track escalated problems and ensure that duplicate alerts aren't re-sent, preventing "notification fatigue."
<img width="1591" height="600" alt="image" src="https://github.com/user-attachments/assets/7d35433c-0c3f-407b-ad2d-697e3a739d1c" />

---


### 📈 The "Home Run" (The Results)
By "spackling" the gap between the enterprise report and the staff, we achieved:
* **Manager Productivity:** The manager was freed from "Queue Custody," allowing him to fit in **3x as many patient appointments** of his own.
* **Staff Accountability:** By putting the data directly in the hands of the therapists, the "singles" were handled daily, keeping the billing queues clean.
* **Sustainability:** The process is now decentralized and resilient, no longer relying on a single "expert" to interpret the Kraken.















