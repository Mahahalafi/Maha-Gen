# My Final Project

## Project Name
**Meeting Follow-up Assistant**

## Idea Selected
**Meeting Follow-up Assistant**

## Problem Statement
After meetings, notes are often unstructured and hard to review, lack clear owners or deadlines, take a long time to turn into a professional summary, and can miss important decisions or follow-up actions.

This assistant turns raw meeting notes into clear, organized follow-up documentation. It cuts manual effort and makes sure outcomes are properly documented.

## Target Users
- Team leads and managers who run recurring review meetings
- Project and service coordinators who track owners, deliverables and deadlines
- Network and operations teams running MSP, SLA/KPI, and vendor performance reviews

## R-C-T-F Prompt

```
ROLE:
You are a professional Meeting Follow-up Assistant specialized in converting unstructured workplace meeting notes into clear, accurate, and actionable meeting documentation.

CONTEXT:
I will provide raw meeting notes that may contain incomplete sentences, discussions, decisions, action items, names, deadlines, and unresolved questions. Your job is to organize the information without changing its meaning.

TASK:
Analyze the meeting notes and create:
1. Meeting Summary – a concise overview of the meeting.
2. Key Discussion Points – the main topics discussed.
3. Decisions Made – only decisions that were explicitly agreed upon.
4. Action Items – Action, Owner, Deadline, Status.
5. Open Questions / Pending Items – topics that still need clarification or follow-up.
6. Follow-up Email – a professional email summarizing the meeting and highlighting required actions.

RULES:
- Do not invent or assume information.
- Do not create owners or deadlines that are not mentioned.
- If an owner or deadline is missing, write "Not specified."
- Clearly distinguish between a discussion point and an actual decision.
- Keep all numbers, dates, names, and facts exactly as provided.
- If the notes contain conflicting information, flag it instead of choosing one version.

FORMAT:
- Use clear headings for each of the six sections.
- Present Action Items as a table: Action | Owner | Deadline | Status.
- Keep the output professional, concise, and easy to scan.
- Write the email with a subject line, greeting, body, and sign-off.
```

## Sample Input

```
Meeting date: Wednesday, 30 September 2026, 11:00 AM

1. MSP & Governance Alignment – Owner: Khaled
   * MSP to present the current alignment points, open gaps, and required actions.
2. Risk Register Update – Owner: Hala
   * Review new and existing risks.
   * Status of mitigation actions and escalations.
3. MSP Weekly Performance – Owner: Abdullah
   * Weekly performance overview.
   * Key achievements, challenges, SLA/KPI status, and pending actions.
4. TSS Deliverables – Owner: Alzuair
   * Status of committed TSS reports, recommendations, and pending deliverables.
5. RMA Deliverables – Owner: Sherif Nour – Amgad Elwakeel
   * RMA status, aging cases, pending replacements, and major concerns.
6. BCS Deliverables – Owner: AlZuair
   * Review committed BCS deliverables, progress, delays, and required support.

Please ensure the respective owners are prepared with the latest status, pending actions, and target completion dates.
All owners are required to attend the meeting.
```

## Sample Output

### 1. Meeting Summary
The MSP Governance & Deliverables Review is scheduled for Wednesday, 30 September 2026, 11:00 AM. It covers six items: MSP governance alignment, risk register, MSP weekly performance, and TSS, RMA and BCS deliverables. All owners must attend and come prepared with the latest status, pending actions, and target completion dates.

### 2. Key Discussion Points
- **MSP & Governance Alignment: ** alignment points, open gaps, required actions
- **Risk Register Update: ** new and existing risks, mitigation status, escalations
- **MSP Weekly Performance: ** achievements, challenges, SLA/KPI status, pending actions
- **TSS Deliverables: ** committed reports, recommendations, pending deliverables
- **RMA Deliverables: ** RMA status, aging cases, pending replacements, major concerns
- **BCS Deliverables: ** progress, delays, required support

### 3. Decisions Made
No decisions are recorded in the notes. The items above are agenda topics for discussion.

### 4. Action Items

| Action | Owner | Deadline | Status |
|---|---|---|---|
| Present MSP alignment points, open gaps, and required actions | Khaled | 30 Sep 2026, 11:00 AM (meeting) | Not specified |
| Present risk register update | Hala | 30 Sep 2026, 11:00 AM (meeting) | Not specified |
| Present MSP weekly performance, including SLA/KPI status | Abdullah | 30 Sep 2026, 11:00 AM (meeting) | Not specified |
| Present TSS deliverables status | Alzuair | 30 Sep 2026, 11:00 AM (meeting) | Not specified |
| Present RMA status, aging cases, and pending replacements | Sherif Nour – Amgad Elwakeel | 30 Sep 2026, 11:00 AM (meeting) | Not specified |
| Present BCS deliverables progress and required support | AlZuair | 30 Sep 2026, 11:00 AM (meeting) | Not specified |
| Attend the meeting, prepared with latest status, pending actions, and target completion dates | All owners | 30 Sep 2026, 11:00 AM | Not specified |

### 5. Open Questions / Pending Items
- How many gaps opened and remining with No action
- How many aged Cases related to RMA & TSS.

### 6. Follow-up Email

**Subject:** MSP Governance & Deliverables Review – Wednesday, 30 September 2026, 11:00 AM

Dear All,

The MSP Governance & Deliverables Review is scheduled for **Wednesday, 30 September 2026, at 11:00 AM**. Attendance is required for all owners.

**Agenda and owners: **
1. MSP & Governance Alignment – Khaled
2. Risk Register Update – Hala
3. MSP Weekly Performance – Abdullah
4. TSS Deliverables – AlZuair
5. RMA Deliverables – Sherif Nour
6. BCS Deliverables – AlZuair

**Required action: ** Each owner is kindly requested to come prepared with:
- Latest status
- Pending actions
- Target completion dates

Thank you for your cooperation.

Best regards,
Maha Alhalafi

## Safety Checklist
Before using the output, I checked:
- **Accuracy:** All names, dates and topics match the original notes.
- **No invented information:** No decisions, owners or deadlines were added that weren't in the notes.
- **Missing data:** Empty fields are marked "Not specified" instead of guessed.
- **Conflicts flagged:** The name spelling difference was flagged, not silently corrected.
- **Decisions vs. discussion:** Agenda items were not presented as decisions.
- **Confidentiality:** The notes contain no passwords, customer data or sensitive financial details, and I avoid sharing confidential information with AI tools.
- **Human review:** I reviewed and approved the email before sending it.

## Reflection
- A clear R-C-T-F structure makes the AI's output consistent and easy to reuse.
- Adding explicit rules ("do not invent," "write Not specified," "flag conflicts") was the most important improvement. Without them, the AI can turn agenda items into fake decisions or add deadlines on its own.
- AI output still needs human review. I found date, name and owner inconsistencies that had to be confirmed.
- The assistant saves real time on recurring meetings like MSP and SLA reviews and makes follow-up actions easier to track.


