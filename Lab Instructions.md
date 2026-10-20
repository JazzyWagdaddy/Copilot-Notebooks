# Microsoft Copilot Notebooks

> A hands-on lab for learning the complete core workflow: create a notebook, add trusted references, ask grounded questions, shape responses with instructions, create useful outputs, and understand sharing, limits, and advanced features.

## Lab at a glance

| Item | Details |
|---|---|
| Audience | New Copilot Notebooks learners |
| Duration | 30 minutes, plus additional challenges |
| Format | Self-paced, hands-on |
| Difficulty | Beginner |
| Product | Microsoft Copilot Notebooks |
| Outcome | A working notebook that answers questions and creates content from a curated set of references |

## What you will learn

By the end of the lab, you will be able to:

1. Explain what a Copilot Notebook is and when to use one.
2. Create and name a notebook.
3. Add, inspect, and remove references.
4. Ask questions that are grounded in notebook content.
5. Improve results with follow-up prompts and notebook instructions.
6. Create a reusable project update from the references.
7. Recognize sharing and permission implications.
8. Identify advanced features, licensing differences, and current limitations.

## The mental model

A Copilot Notebook is a **scoped AI workspace**. You choose the references, and Copilot uses that curated context to answer questions, summarize, analyze, and draft content.

Think of the workflow as:

```text
Create a notebook
        ↓
Add trusted references
        ↓
Ask grounded questions
        ↓
Refine with follow-up prompts and instructions
        ↓
Create and collaborate on useful outputs
        ↓
Come back to the workspace to continue future work on the same content and pickup right where you left off
```

---

## Before you begin

### Required

- A Microsoft account that can access Copilot Notebooks.
- A SharePoint or OneDrive service plan to create notebooks.
- Access to the Microsoft Copilot app from your desktop.
- Two sample files :
  
  [Promotion Plan for Chai Tea in Latin America](https://go.microsoft.com/fwlink/?linkid=2269126)
  
  [Market Analysis Report for Mystic Spice Premium Chai Tea](https://go.microsoft.com/fwlink/?linkid=2268826)

  **Download both files and save them to your OneDrive folder before you continue.**

### Feature availability

Copilot Notebook capabilities vary by account, license, organization policy, platform, and rollout status. If a button used in an optional exercise is unavailable, read the exercise and continue. The core create → reference → prompt workflow should remain the focus.

### Responsible-use reminder

- Use content you are permitted to access.
- Check generated answers against their cited or linked references.
- Do not treat an AI-generated answer as automatically correct.
- Obtain consent before recording or transcribing people.
- Review file permissions before sharing a notebook.

---

# Lab Time!

## Task 1: Create your first Notebook

### Scenario

You are joining the fictional **Northwind Trail** team. The team is preparing for expansion into Latin america. You need to understand the project quickly and prepare a concise status update.

### Steps

1. Ensure that you have downloaded the required files, then sign in to the Microsoft Copilot app on your desktop.
2. In the left navigation, open **Notebooks**.
   - If you do not see it, check the app launcher.
3. Select **All notebooks**, and then select **New notebook**.
4. Name it and copying and pasting this text:
   ```text
   Northwind Trail Launch Lab
   ```

6. Notice the options to add content or previous chats to this Notebook.  When ready, click **Create**.
7. Keep the notebook open for the rest of the lab.

### Check your work

You should see a new notebook with an area for references and a Copilot message box.

### What you learned

A notebook is most useful when it is organized around a defined project, task, decision, or learning goal—not as an unbounded collection of unrelated files.

---

## Task 2: Add and manage references/content

***Please note that in some UI version files you add are called REFERENCES and in other versions they are called CONTENT.  Both are the same***

### Steps

1. In your notebook, on the right-hand side of the screen, select the plus symbol next to **In Northwind Trail Launch Lab** and then choose **Add content**.  Please note that your UI may say **Add references**.
2. Throughout this lab, you craft prompts that reference these files. 
3. Choose **Upload** and upload these files:
   
   *Promotion Plan for Chai Tea in Latin America*
   
   *Market Analysis Report for Mystic Spice Premium Chai Tea*
   
5. Confirm that both files appear in the content/references section of your Notebook.

### Explore other reference/content methods

Open **Add references** or **Add content** again and review the additional options available to you:

- *Work Content* - this launches the Object Picker you saw in earlier labs where you can reference work files, meetings, emails, SharePoint sites, and Team Chats.
- *Upload* - upload files from your local or network drives
- *Links* - Add links to websites as content
- *OneDrive* - Provide a link to a OneDrive folder or individual files from your Most Recently Used (MRU) list from OneDrive

***Do not add confidential or unrelated material just to complete the exercise.***

### Key concept: the reference boundary

The references define the notebook's working context. Copilot does not automatically treat every file, email, chat, or website you can access as part of this notebook. Adding a specific file directly is the safest way to ensure it is included in the notebook's grounding set.

### Check your work

Your notebook should show **two references**.

---

## Task 3: Ask grounded questions

Paste the following prompt in the Chat window:

```

Using only the references in this notebook, summarize the materials in five bullets.
Include the target users, goal, proposed timing, success measures, and the most important customer concern.
After each bullet, identify which reference supports it.

```

Since Copilot will use only the documents in the Notebook as the source and provide a response, ask the following:

```
Which requested details are missing, unclear, or conflicting across the references?
Do not guess. Create a table with the columns Detail, What the references say, Gap or conflict, and Recommended follow-up question.
```

Finally, ask:

```
What evidence in the notebook supports the recommendation to prioritize offline route access? Quote only short phrases and explain how each phrase supports the recommendation.
```

### Observe

Look for these behaviors:

- The answer should focus on the two added references.
- Copilot should distinguish stated facts from gaps.
- A strong response should avoid inventing owners, dates, budgets, or metrics.
- Reference indicators should let you inspect the supporting content.

### Prompt pattern to remember

Use this reusable formula:

```text
Using [scope], perform [task].
Include [required fields].
Use [format].
Apply [quality rule].
```

Example:

```
Using only this notebook, compare the proposed pilot with the customer feedback. Use a table with Alignment, Tension, and Open question columns. Do not fill missing details with assumptions.
```

---

## Task 4: Set notebook instructions

Notebook instructions let you define response preferences that should apply throughout the notebook.

### Steps

1. Open the notebook's **More options** menu.  This can be in different places based upon your UI version.  Where you see the name of the project, click the down arrow.  Alternatively, you may need to click on the three dots near the green shield icon.
2. Select **Instructions**.
4.  Enter:

   ```
   Write for a project manager who is new to the initiative. Use plain language, short sections, and concise tables. Separate confirmed facts from assumptions and open questions. Never invent a date, owner, budget, or metric that is not present in the references.
   ```

5. Save the instructions.
6. Re-run this shorter prompt:

   ```
   Give me a launch-readiness assessment.
   ```

### Compare

Did the result now:

- Use a clearer project-management structure?
- Separate facts from open questions?
- Avoid unsupported specifics?
- Reflect the intended audience and tone?

### What you learned

Use **notebook instructions** for durable behavior within the Notebook such as audience, tone, formatting, terminology, and rules. Use the individual prompt for the task-specific request.  Remember that these instructions are specific to this notebook and will not apply to any other notebooks nor chats outside this notebook.

---

## Task 5: Create a useful deliverable

Start a new chat (the plus button near the top) and paste:

```
Create a project update titled "Northwind Trail Pilot — Readiness Update."

Include:
1. A two-sentence executive summary.
2. A table of confirmed scope, target users, timing, and success measures.
3. The top three customer needs, with supporting evidence.
4. A Risks and Open Questions table with columns Item, Why it matters, Evidence available, and Next action.
5. Three decisions the team should make next.

Use only this notebook's references. Label any unsupported information as "Not found in references."
```

### Check your work

Your update should contain all five requested sections and clearly expose information gaps instead of hiding them.

---

## Task 6: Share safely and finish

### Sharing inspection

1. Close any windows from previous tasks and then open a new chat (this keeps the screen less cluttered).  Select **Share** or **Add Members** depending on your UI version.
2. Review the invite experience, and only send an invitation to an approved lab partner or friend.  Do not share this broadly across the company or to any specific groups
3. Before sharing, answer:
   - Do I have permission to share every referenced file?
   - Should the people I invite have access to this content?  Do they already have access to this content today?
   - Could sharing the notebook grant or request access to linked content?
   - Does the recipient have the license needed for premium reference types?
   - Is edit access appropriate?

## Your Final Task: Create a Real Notebook   

Repeat these steps and create a Notebook that is specific to you, your role, and what you do on a regualr basis.  Add a folder from OneDrive or a website

## Challenge exercises

Complete these steps on the Northwind Trail Launch Lab or your own personal Notebook.

### Challenge 1 — Test the grounding boundary

Ask a question whose answer does not appear in either reference.

A good response should state that the budget is not available in the references.

### Challenge 2 — Change the evidence set

Temporarily remove one of the files then ask a previous prompt. Compare the result with the earlier answer. Re-add the reference afterward.

### Challenge 3 — Create an executive version

Change the notebook instructions to:

```text
Write for an executive audience. Lead with the decision required, limit responses to 150 words unless asked otherwise, and highlight risks in a table.
```

Re-run the prompt and compare the output.

## Challenge 4 — Build a reusable prompt

Adapt this template to your own project:

```text
Using only this notebook, create a [deliverable] for [audience].
Include [required sections].
Use [format and length].
Distinguish confirmed facts, assumptions, conflicts, and missing information.
For each recommendation, explain which references support it.
```
