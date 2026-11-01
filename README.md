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
**Stop Buying Licenses for Single-Use Tools [When You Already Own the Solution](https://youtu.be/u3vxyO36KzA)** (Redirect to YouTube)

Modern enterprises are often "Tool Rich but Solution Poor." Many organizations pay for expensive, single-use software licenses to bridge operational gaps that their existing desktop tools could already handle—if they had someone with the creativity to connect them.

* **The Problem:** Teams often advocate for $50k+/year "middleware" or "project management" subscriptions just to get two different data sources to talk to one another. 
* **The Reality:** 99% of today's enterprise employees already have a world-class development environment sitting on their taskbar.
* **The 'Spackle' Approach:** I specialize in identifying "licensing gaps." Instead of adding another line item to the IT budget, I leverage ubiquitous tools—**VBA, Power Query, SQL, Python**—to build custom, zero-marginal-cost solutions that live where the staff already works. I use no-cost, open-source tools, and open-source computing resources when I need a bigger hammer! (My current organization spent a grand total of $0 on software for any of the projects featured in my Git)

> **The Value Proposition:** I don't just solve technical problems; I solve **budgetary** ones. I make the tools you are *already paying for* work harder, ensuring your tech stack is lean, integrated, and high-ROI.





### changes below


# Enterprise_Quality_Spackle 🛠️

> **The Philosophy:** Four singles can equal a home run. Small, targeted improvements are often easier to adopt, more sustainable, and more valuable than a large project that nobody uses.

## Executive Summary

This case study describes a last-mile workflow solution for a technically sophisticated but difficult-to-use rehabilitation billing report.

The original enterprise report combined multiple SQL queries, approximately 400 data elements, 200 calculation variables, and 68 formatting rules. It was analytically powerful but difficult to use in a mobile, frontline rehabilitation workflow.

I built a VBA-based workflow that:

- Translated complex visual flags into plain-language status updates
- Distributed individualized work queues to more than 20 therapists
- Maintained a tracking database for escalated issues
- Prevented duplicate notifications
- Reduced dependence on a single manager
- Helped complete a site-wide cleanup effort in less than one week

The project illustrates a recurring informatics principle:

> A technically excellent system can still fail if it does not fit the user’s physical environment, workflow, or cognitive load.

---

## Case Study: The Kraken

### VBA as Middleware: Taming a Complex Enterprise Report

In large organizations, enterprise reporting teams and frontline users often work under very different conditions. A report can be technically sophisticated and analytically comprehensive while still being difficult to use in daily operations.

This is the story of **The Kraken**—a complex rehabilitation billing report that contained valuable information but placed too much interpretive and administrative burden on the end user.

## The Problem: Complex Data, Difficult Workflow

Physical, occupational, and speech-language therapy billing can create significant operational challenges for hospitals providing these services.

Claims may require:

- Appropriate orders
- Active encounters
- Current treatment objectives
- Accurate documentation
- Regulatory compliance
- Consistent follow-up across many therapy sessions

Therapy episodes can extend across dozens of encounters over many months. Orders may become stale, treatment objectives may change, and unresolved documentation problems can remain hidden until a claim is delayed or rejected.

Frontline therapists and rehabilitation managers may also have limited administrative time to investigate these problems. As unresolved items accumulate, review queues grow and revenue-cycle work becomes increasingly difficult to manage.

### The Original Enterprise Report

A three-person headquarters reporting team developed a sophisticated report to identify potential problems in the rehabilitation billing workflow.

The report used:

- Multiple integrated SQL queries
- Approximately 400 data elements
- Approximately 200 custom calculation variables
- Sixty-eight formatting rules
- Numerous conditional combinations
- Color-coded flags and a detailed visual legend

The report was technically ambitious and contained substantial analytical value.

However, its structure made it difficult for frontline users to interpret and distribute the information efficiently.

![Example of the enterprise report](https://github.com/user-attachments/assets/7504edee-5f66-4996-8644-4eca8ef136be)

## The Scale

The report used multiple integrated queries to retrieve and combine approximately 400 table elements.

[View the integrated SQL queries](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/HQ_SQL_KRAKEN)

![Integrated query structure](https://github.com/user-attachments/assets/f08ebdc8-0161-4c1d-ab1b-a507eb1cb2c5)

## The Complexity

The report included approximately 200 custom calculation variables.

![Custom calculation variables](https://github.com/user-attachments/assets/72d021c5-f03b-4aff-8efc-aac33205532b)

Many of those variables also contained substantial internal logic and dimensional complexity.

![Calculation complexity](https://github.com/user-attachments/assets/bca63865-f004-43e6-bcf5-f15d8be2d52b)

The report also included 68 formatting rules that combined multiple logical conditions into a visual flagging system.

![Formatting rules](https://github.com/user-attachments/assets/baf08218-9ff1-4593-a425-410419880413)

The resulting report used a detailed color-coded legend to communicate the meaning of its many status conditions.

![Flagging legend](https://github.com/user-attachments/assets/f517b96c-bb0e-48cb-bccf-76de44bd1eb0)

## The Usability Problem

The resulting output was technically comprehensive but difficult to use in the actual rehabilitation workflow.

The primary user was not working from a fixed office workstation with multiple monitors. The manager was frequently moving through clinical areas and working from a 15-inch laptop.

The wide-format report required the user to:

- Scroll horizontally to locate relevant columns
- Keep track of dates, names, and numbers manually
- Interpret complex color-coded conditions
- Navigate merged cells and hidden rows
- Work around inconsistent column widths
- Separate relevant items for distribution to individual therapists

![Complex report output](https://github.com/user-attachments/assets/9ca736b5-197e-4b43-a3fd-04873e5b2151)

The problem was not a lack of information. The problem was that the information was not presented in a form that matched the user’s physical environment or daily workflow.

![Frontline usability challenge](https://github.com/user-attachments/assets/86769b7e-b482-4101-ab6d-65c50ecfe73d)

## The Operational Cost

Managing the queues became a substantial recurring responsibility for the rehabilitation manager.

This created several risks:

- Work remained concentrated with one person
- Revenue-integrity activity slowed when the manager was unavailable
- Therapists did not always receive actionable information directly
- Duplicate alerts could contribute to notification fatigue
- A technically valuable report was underused because it required too much manual interpretation

Re-engineering the enterprise report would have required significant time, coordination, and cost. A lightweight last-mile solution offered a faster path to operational value.

---

## The Solution: The Spackle Strategy

Rather than replace the enterprise report, I built a workflow layer that translated its output into a more usable process.

The solution used existing tools:

- VBA
- Excel
- Outlook
- SQL-generated report data
- A relational tracking database

The goal was not to compete with the enterprise reporting system. The goal was to carry its information across the last mile to the people responsible for acting on it.

[View the VBA workflow](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/KRAKEN_SLAYER_VBA)

## Technical Architecture

- **Input:** Enterprise SQL report exported to Excel
- **Processing:** VBA reads report rows, evaluates status flags, and translates formatting logic
- **Translation:** Complex visual conditions are converted into plain-language status messages
- **Distribution:** Individualized work queues are prepared and distributed through Outlook
- **Tracking:** A master database records escalated issues and suppresses duplicate notifications
- **Users:** Rehabilitation manager and more than 20 therapists
- **Software environment:** Existing enterprise tools, with no additional software licensing required for the workflow

### 1. Plain-Language Translation

The VBA process reads the report’s color-coded flags and translates them into actionable status updates.

This removes the need for each user to interpret the report’s underlying formatting logic independently.

![Plain-language status translation](https://github.com/user-attachments/assets/d2471a24-3ac9-424c-b9ee-c39f2c53772b)

### 2. Automated Distribution

Instead of requiring one manager to manually sort and distribute rows, the process creates individualized work queues for more than 20 therapists and distributes them through Outlook.

![Automated distribution](https://github.com/user-attachments/assets/ade0af23-14ba-42eb-8827-dc48f631c301)

### 3. Revenue-Integrity Tracking

The workflow maintains a master database of escalated problems.

This allows the process to:

- Track unresolved issues
- Prevent duplicate alerts
- Reduce notification fatigue
- Separate previously combined problem types
- Support targeted batching and resolution sprints
- Preserve continuity when the primary manager is unavailable

![Revenue-integrity tracking database](https://github.com/user-attachments/assets/7d35433c-0c3f-407b-ad2d-697e3a739d1c)

---

## Results

By adding a workflow layer between the enterprise report and frontline staff, the project produced several operational improvements.

### Manager Capacity

The rehabilitation manager reported approximately three times the available capacity for patient appointments after queue-management responsibilities were reduced.

### Staff Accountability

Actionable information was delivered directly to the therapists responsible for resolving the underlying issues.

This allowed smaller items to be handled continuously rather than accumulating in a centralized queue.

### Faster Cleanup

A corporate cleanup directive that had taken other sites months to complete was completed at this site in less than one week.

### Sustainability

The process became less dependent on a single expert who understood how to interpret and distribute the original report.

The workflow was more decentralized, repeatable, and resilient.

---

## Key Informatics Lessons

### 1. Technical sophistication is not the same as usability

A report can contain excellent data and logic while still failing to support the user’s actual workflow.

### 2. Last-mile design matters

The final step between data production and user action can determine whether an analytical system creates value.

### 3. Workflow fit is a technical requirement

A solution must account for:

- The user’s physical environment
- Screen size and mobility
- Available administrative time
- Cognitive load
- Distribution responsibilities
- The frequency of required action

### 4. Small interventions can produce large operational gains

A targeted workflow layer can sometimes unlock value from an existing enterprise system without replacing the underlying platform.

### 5. Decentralization improves resilience

When actionable work is distributed to the people responsible for resolving it, the process becomes less dependent on a single manager or subject-matter expert.

---

## Case Study: The Hidden Swiss Army Knife

### Stop Buying Single-Use Tools When Existing Tools Can Do the Work

[Watch the related video](https://youtu.be/u3vxyO36KzA)

Modern enterprises are often **tool-rich but solution-poor**. Organizations may purchase expensive middleware or project-management platforms to address integration problems that existing desktop and open-source tools could solve with the right design.

Many teams already have capable tools available, including:

- Excel and VBA
- Power Query
- SQL
- Python
- Open-source data and computing tools

The challenge is often not the absence of technology. It is the absence of someone who can connect the tools to the workflow.

## The Spackle Approach

I specialize in identifying practical gaps between existing systems and frontline needs.

Rather than automatically introducing another platform, I evaluate whether the current environment can be extended through:

- VBA automation
- Power Query transformations
- SQL reporting
- Python-based analysis
- Relational tracking databases
- Lightweight workflow interfaces
- Open-source tools where appropriate

The objective is to avoid unnecessary software-license costs while making the existing technology stack more useful, integrated, and sustainable.

> **The Value Proposition:** I do not simply solve technical problems. I solve workflow and budget problems by helping organizations get more value from tools they already own.

---

## Privacy and Security

This repository does not contain patient-identifiable information, production credentials, or unrestricted production database extracts.

Screenshots, examples, and demonstrations have been redacted, simulated, or recreated for portfolio purposes where necessary.

Any production implementation should be reviewed according to applicable organizational privacy, security, data-governance, and change-management requirements.

---

## Repository Contents

- [Enterprise SQL query examples](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/HQ_SQL_KRAKEN)
- [VBA workflow automation](https://github.com/kirk-allen-ryan/Enterprise_Quality_Spackle/blob/main/KRAKEN_SLAYER_VBA)
- Supporting screenshots and workflow documentation
- Case-study narrative and implementation notes

---

## Final Takeaway

The most valuable solution is not always the largest or most technically elaborate one.

Sometimes the best intervention is a carefully designed layer between a powerful enterprise system and the people who need to use its output.

**The Kraken produced the information.  
The Spackle made the information usable.**








