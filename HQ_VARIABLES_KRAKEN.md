**DaysSinceLastNote** 
  =DaysBetween([LAST CE];LastExecutionDate())

---

**Discipline by Form** 
  =If [Form Description] InList("OT Communication/Contact Form";"OT Missed Minutes";"OT Orthotic Assessment Form";"OT Outpatient Pediatric Daily Doc";"OT Outpatient Pediatric Discharge Summary";"OT Outpatient Pediatric Evaluation";"OT Outpatient Pediatric Progress Note";"OT Outpatient Time Spent With Patient";"Outpatient OT Plan of Care Signature Form") Then "OT"

ElseIf [Form Description] InList("Outpatient PT Plan of Care Signature Form";"PT Communication/Contact Form";"PT Missed Minutes";"PT Outpatient Brief Evaluation";"PT Outpatient Ped Daily Documentation";"PT Outpatient Pediatric Discharge Summary";"PT Outpatient Pediatric Evaluation";"PT Outpatient Pediatric Progress Note";"PT Outpatient Time Spent With Patient") Then "PT"

ElseIf [Form Description] InList("Outpatient SLP Plan of Care Signature Form";"SLP Communication/Contact Form";"SLP Missed Minutes";"SLP Outpatient Ped Daily Documentation";"SLP Outpatient Pediatric Discharge Summary";"SLP Outpatient Pediatric Evaluation";"SLP Outpatient Pediatric Progress Note";"SLP Outpatient Time Spent With Patient";"SLP Pediatric Dysphagia Evaluation") Then "SLP"

---

**ENC**
  = If ([Encounter Type]="Intake")Then("INTK") 
ElseIf ([Encounter Type]="ASC")Then("ASC") 
ElseIf ([Encounter Type]="Between Visit")Then("BV") 
ElseIf ([Encounter Type]="Camp")Then("CAMP")
ElseIf ([Encounter Type]="Inpatient")Then("IP")
ElseIf ([Encounter Type]="IRU Screening")Then("IRU-S")
ElseIf ([Encounter Type]="Observation")Then("OBS") 
ElseIf ([Encounter Type]="Outpatient Clinic")Then("OP-C") 
ElseIf ([Encounter Type]="Outpatient Rehab")Then("OP-R") 
ElseIf ([Encounter Type]="Outpatient Surgery")Then("OP-S") 
ElseIf ([Encounter Type]="Outpatient")Then("OP") 
ElseIf ([Encounter Type]="Outreach")Then("OTR") 
ElseIf ([Encounter Type]="Outside Prof Svcs")Then("PRO") 
ElseIf ([Encounter Type]="Outside Services")Then("OS") 
ElseIf ([Encounter Type]="PAT")Then("PAT") 
ElseIf ([Encounter Type]="Pre-Admit")Then("PreADM") 
ElseIf ([Encounter Type]="Pre-Recurring")Then("PreRCR") 
ElseIf ([Encounter Type]="Pre-Reg")Then("PreREG") 
ElseIf ([Encounter Type]="Recurring")Then("RCUR") 
ElseIf ([Encounter Type]="Rehab Inpatient")Then("IP-R") 
ElseIf ([Encounter Type]="Subacute")Then("SUB") 
ElseIf ([Encounter Type]="Telehealth")Then("Tel-H")
ElseIf ([Encounter Type]="Telemedicine")Then("Tel-M") 
ElseIf ([Encounter Type]=" ")Then("NONE!") 
ElseIf ([Encounter Type]="")Then("NONE!")
Else [Encounter Type]

---

**ENC Age**
  =DaysBetween([Admit Date & Time];LastExecutionDate())

---

**FIN OT**
  =If [discipline on FIN = OT]=1 Then [Financial Number]

---

**FIN PT**
  =If [discipline on FIN = PT]=1 Then [Financial Number]

---

**FIN SLP**
  =If [discipline on FIN = SLP]=1 Then [Financial Number]

---

**HOS**
  =If [Person Location- Facility (Curr)]="BOSTON" Then "BOS"
ElseIf [Person Location- Facility (Curr)]="CANADIAN" Then "CAN"
ElseIf [Person Location- Facility (Curr)]="CHICAGO" Then "CHI"
ElseIf [Person Location- Facility (Curr)]="CINCINNATI" Then "CIN"
ElseIf Match([Person Location- Facility (Curr)];"ERI*") Then "ERI"
ElseIf [Person Location- Facility (Curr)]="GALVESTON" Then "GAL"
ElseIf [Person Location- Facility (Curr)]="GREENVILLE" Then "GRN"
ElseIf [Person Location- Facility (Curr)]="HONOLULU" Then "HON"
ElseIf [Person Location- Facility (Curr)]="HOUSTON" Then "HOU"
ElseIf [Person Location- Facility (Curr)]="LEXINGTONMC" Then "LXT"
ElseIf Match([Person Location- Facility (Curr)];"LXT*") Then "LXT" 
ElseIf [Person Location- Facility (Curr)]="LEXINGTON" Then "LXT"
ElseIf [Person Location- Facility (Curr)]="PASADENAMC" Then "PAS" 
ElseIf Match([Person Location- Facility (Curr)];"PAS*") Then "PAS"
ElseIf [Person Location- Facility (Curr)]="LOS ANGELES" Then "PAS"
ElseIf [Person Location- Facility (Curr)]="NORTHERN CALIFO" Then "NCL"
ElseIf [Person Location- Facility (Curr)]="PHILADELPHIA" Then "PHL"
ElseIf [Person Location- Facility (Curr)]="PORTLAND" Then "POR"
ElseIf [Person Location- Facility (Curr)]="SALT LAKE CITY" Then "SCC"
ElseIf Match([Person Location- Facility (Curr)];"SCC*") Then "SCC"
ElseIf [Person Location- Facility (Curr)]="SHREVEPORT" Then "SHR"
ElseIf [Person Location- Facility (Curr)]="SPOKANE" Then "SPO"
ElseIf [Person Location- Facility (Curr)]="SPRINGFIELD" Then "SPR"
ElseIf [Person Location- Facility (Curr)]="ST. LOUIS" Then "STL"
ElseIf [Person Location- Facility (Curr)]="TAMPA" Then "TPC"
ElseIf [Person Location- Facility (Curr)]="TPC CLINIC" Then "TPC"
ElseIf Match([Person Location- Facility (Curr)];"TPC*") Then "TPC" 
ElseIf [Person Location- Facility (Curr)]="TWIN CITIES" Then "TCC"
ElseIf [Person Location- Facility (Curr)]="TCC FACILITY" Then "TCC"
ElseIf Match ([Person Location- Facility (Curr)];"TCC*") Then "TCC"
Else  Left([Person Location- Facility (Curr)];3)

---

**discipline on FIN = OT**
  =If [Form Description] InList("OT Communication/Contact Form";"OT Missed Minutes";"OT Orthotic Assessment Form";"OT Outpatient Pediatric Daily Doc";"OT Outpatient Pediatric Discharge Summary";"OT Outpatient Pediatric Evaluation";"OT Outpatient Pediatric Progress Note";"OT Outpatient Time Spent With Patient";"Outpatient OT Plan of Care Signature Form";"OT Outpatient Brief Evaluation") Then 1

---

**discipline on FIN = PT**
  =If [Form Description] InList("Outpatient PT Plan of Care Signature Form";"PT Communication/Contact Form";"PT Missed Minutes";"PT Outpatient Brief Evaluation";"PT Outpatient Ped Daily Documentation";"PT Outpatient Pediatric Discharge Summary";"PT Outpatient Pediatric Evaluation";"PT Outpatient Pediatric Progress Note";"PT Outpatient Time Spent With Patient") Then 1

---

**discipline on FIN = SLP**
  =If [Form Description] InList("Outpatient SLP Plan of Care Signature Form";"SLP Communication/Contact Form";"SLP Missed Minutes";"SLP Outpatient Ped Daily Documentation";"SLP Outpatient Pediatric Discharge Summary";"SLP Outpatient Pediatric Evaluation";"SLP Outpatient Pediatric Progress Note";"SLP Outpatient Time Spent With Patient";"SLP Pediatric Dysphagia Evaluation") Then 1

---

**Eval Only OT**
  = If [Element Description]="OT Frequency Rehab"  And [Response Value- Discrete]="Evaluation Only" Then "EO "+ FormatDate([eval only?].[Documentation Date & Time];"M/d/yy")

---  

**POC Ordering Physician Name OT**
  =If [poc form].[Form Description]="Outpatient OT Plan of Care Signature Form" Then [Response Value- Free text] Where([poc form].[Element Description]="Ordering Physician Name")
