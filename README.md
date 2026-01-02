# Enterprise_Quality_Spackle 🛠️

> **The Philosophy:** 4 Singles = 1 Home Run. A series of small wins will often count the same, get more people involved, and are often more sustainable than a "grand slam" project that no one will use.

---

## 🐙 Case Study:'The Kraken'
**VBA as Middleware: How a Monster Report Was Tamed**

In any large organization, there is often a natural tension between HQ technical teams and front-line managers. This is the story of **The Kraken**—an enterprise report so complex it nearly drowned the department it was meant to save.

### 🚩 The Problem: Enterprise Over-Engineering
Our HQ report writers are brilliant and hardworking, but they built a data-science marvel that was a nightmare for end-users.

* **The Backstory:** Physical therapy, Occupational therapy, and Speech-Language therapy billing can be a pain for hospitals that provide these service lines. No bills can go out without orders. No orders can be written without encounters. And therapy can involve dozens of sessions over many months of time, which means that single billing encounters can be stretched over dozens of in-person encounters. Orders become stale. Treatment objectives change. Complicated narratives must be coded and regulations complied with. Busy therapists often not afforded adequate admin time to track down the reasons for current claims that are snagged by problems that got missed a year ago. Review queues mushroom and revenue streams get clogged.

*  **The Solution(?)** SQL scripting to scan EMR databases to gather relevent records, and logical calculations to flag specific combinations of conditions. A 3-person HQ reporting team took on the challenge on October-23, and 79 days later they published their masterpiece...

<img width="512" height="435" alt="image" src="https://github.com/user-attachments/assets/7504edee-5f66-4996-8644-4eca8ef136be" />

---

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

 - That combined a web of potential logical conditions into a single flagging rubric with an amazing technicolor decoding legend that dominated the upper-left of the report

<img width="641" height="516" alt="image" src="https://github.com/user-attachments/assets/f517b96c-bb0e-48cb-bccf-76de44bd1eb0" />

---


* **The Result:** A "monster" output - nicknamed The Kraken. It was genius! Except for one tiny problem...
<img width="1877" height="750" alt="image" src="https://github.com/user-attachments/assets/9ca736b5-197e-4b43-a3fd-04873e5b2151" />

---

* **The REAL Problem?**
* A fundamental non-understanding of a Rehab Manager's day! She's not sitting in an office with a dual-monitor workstation - she's on the floor working with kids...and a 15" laptop. By forcing the output into a single, wide-framed table, it was impossilbe for the constantly-moving laptop user to view all the columns they needed in a single frame. They needed a note pad to jot down dates, names, and numbers as they scrolled side to side using the trackpad, and the tangled mess of merged cells, hidden rows, contorted column widths, and conditional formatting made it impractical for casual users to pull the report apart and distribute it across the team...
<img width="1859" height="737" alt="image" src="https://github.com/user-attachments/assets/86769b7e-b482-4101-ab6d-65c50ecfe73d" />


---


* **The Human Cost:** Managing the queues became almost a full-time job for the Rehab Manager. Revenue integrity stalled whenever the manager was away.

---

### 🛠️ The Solution: The 'Spackle' Strategy
Re-engineering the HQ report would be too expensive and time-consuming. Not to mention the potential for hurt feelings. Instead, I used the tools at hand to get the data over the "last mile" to the customer.

I wrote a [**comprehensive VBA script**](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/KRAKEN_SLAYER_VBA) that transformed this monster into a manageable workflow:
1.  **Decoder Ring:** The script reads the HQ report and automatically decodes the RGB flags into plain English status updates.
   <img width="780" height="227" alt="image" src="https://github.com/user-attachments/assets/d2471a24-3ac9-424c-b9ee-c39f2c53772b" />

2.  **Automated Distribution:** Instead of one person manually sorting rows, the script parses the data and distributes individual queues to the **20+ therapists** via Outlook.
   <img width="1519" height="203" alt="image" src="https://github.com/user-attachments/assets/ade0af23-14ba-42be-8827-dc48f631c301" />

3.  **Revenue Integrity Master DB:** The script maintains a master database to track escalated problems and ensure that duplicate alerts aren't re-sent, preventing "notification fatigue." Specific problems that had been previously combined into compounded formatting rules could be atomized and resolved by specific type, unlocking the efficiency of batching and sprints. The slow trickle of desireable outcomes soon became a flood. A corporate "clean-up" directive that took other sites months to complete was accomplished in less than a week...
<img width="1591" height="600" alt="image" src="https://github.com/user-attachments/assets/7d35433c-0c3f-407b-ad2d-697e3a739d1c" />

---


### 📈 The "Home Run" (The Results)
By "spackling" the gap between the enterprise report and the staff, we achieved:
* **Manager Productivity:** The manager was freed from "Queue Custody," allowing him to fit in **3x as many patient appointments** of his own.
* **Staff Accountability:** By putting the data directly in the hands of the therapists, the "singles" were handled daily, keeping the billing queues clean.
* **Sustainability:** The process is now decentralized and resilient, no longer relying on a single "expert" to interpret the Kraken.

## 🛠️ Case Study: The 'Hidden' Swiss Army Knife
**Stop Buying Licenses for Single-Use Tools When You Already Own the Solution**

Modern enterprises are often "Tool Rich but Solution Poor." Many organizations pay for expensive, single-use software licenses to bridge operational gaps that their existing desktop tools could already handle—if they had someone with the creativity to connect them.

* **The Problem:** Teams often advocate for $50k+/year "middleware" or "project management" subscriptions just to get two different data sources to talk to one another. 
* **The Reality:** 99% of today's enterprise employees already have a world-class development environment sitting on their taskbar.
* **The 'Spackle' Approach:** I specialize in identifying "licensing gaps." Instead of adding another line item to the IT budget, I leverage ubiquitous tools—**VBA, Power Query, SQL, Python**—to build custom, zero-marginal-cost solutions that live where the staff already works. I use no-cost, open-source tools, and open-source computing resources when I need a bigger hammer! (My current organization spent a grand total of $0 on software for any of the projects featured in my Git)

> **The Value Proposition:** I don't just solve technical problems; I solve **budgetary** ones. I make the tools you are *already paying for* work harder, ensuring your tech stack is lean, integrated, and high-ROI.















