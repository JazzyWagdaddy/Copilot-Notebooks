# Microsoft Copilot Notebooks in 20 Minutes

> A hands-on beginner lab for learning the complete core workflow: create a notebook, add trusted references, ask grounded questions, shape responses with instructions, create useful outputs, and understand sharing, limits, and advanced features.

## Lab at a glance

| Item | Details |
|---|---|
| Audience | New Copilot Notebooks learners |
| Duration | 20 minutes |
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
```

Copilot Notebooks is available in two connected experiences:

- **Microsoft Copilot app:** a lightweight notebook experience.
- **OneNote:** a fuller workspace with features such as the generated Overview page and, depending on availability, quick-create experiences.

The same notebook can be opened from either experience.

---

## Before you begin

### Required

- A Microsoft account that can access Copilot Notebooks.
- A SharePoint or OneDrive service plan to create notebooks.
- Access to the Microsoft Copilot app at [m365.cloud.microsoft](https://m365.cloud.microsoft).
- The two sample files in this repository:
  - [`lab-files/project-brief.md`](lab-files/project-brief.md)
  - [`lab-files/customer-feedback.md`](lab-files/customer-feedback.md)

### Feature availability

Copilot Notebook capabilities vary by account, license, organization policy, platform, and rollout status. If a button used in an optional exercise is unavailable, read the exercise and continue. The core create → reference → prompt workflow should remain the focus.

### Responsible-use reminder

- Use content you are permitted to access.
- Check generated answers against their cited or linked references.
- Do not treat an AI-generated answer as automatically correct.
- Obtain consent before recording or transcribing people.
- Review file permissions before sharing a notebook.

---

# The 20-minute lab

## 0:00–2:00 — Task 1: Create your first notebook

### Scenario

You are joining the fictional **Northwind Trail** team. The team is preparing a pilot for a mobile route-planning experience. You need to understand the project quickly and prepare a concise status update.

### Steps

1. Sign in to the Microsoft Copilot app.
2. In the left navigation, open **Notebooks**.
   - If you do not see it, check the app launcher.
3. Select **All notebooks**, and then select **New notebook**.
4. Name it:

   ```text
   Northwind Trail Launch Lab
   ```

5. Keep the notebook open for the rest of the lab.

### Check your work

You should see a new notebook with an area for references and a Copilot message box.

### What you learned

A notebook is most useful when it is organized around a defined project, task, decision, or learning goal—not as an unbounded collection of unrelated files.

---

## 2:00–5:00 — Task 2: Add and manage references

### Steps

1. Download or clone this repository.
2. In your notebook, select **Add references**.
3. Upload:
   - `project-brief.md`
   - `customer-feedback.md`
4. Confirm that both files appear in the notebook's references.
5. Open or preview each reference if your experience supports it.

### Optional: explore other reference methods

Open **Add references** again and identify which options are available to you:

- Search suggested work content
- Upload a file
- Add a OneDrive file or folder
- Add a SharePoint site, library, or folder
- Add a public web link
- Drag and drop a file
- Add an email or meeting, depending on license

Do not add confidential or unrelated material just to complete the exercise.

### Key concept: the reference boundary

The references define the notebook's working context. Copilot does not automatically treat every file, email, chat, or website you can access as part of this notebook. Adding a specific file directly is the safest way to ensure it is included in the notebook's grounding set.

### Check your work

Your notebook should show **two references**.

---

## 5:00–9:00 — Task 3: Ask grounded questions

Paste the following prompt:

```text
Using only the references in this notebook, summarize the Northwind Trail pilot in five bullets. Include the target users, goal, proposed timing, success measures, and the most important customer concern. After each bullet, identify which reference supports it.
```

Review the response, then ask:

```text
Which requested details are missing, unclear, or conflicting across the references? Do not guess. Create a table with the columns Detail, What the references say, Gap or conflict, and Recommended follow-up question.
```

Finally, ask:

```text
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

```text
Using only this notebook, compare the proposed pilot with the customer feedback. Use a table with Alignment, Tension, and Open question columns. Do not fill missing details with assumptions.
```

---

## 9:00–12:00 — Task 4: Set notebook instructions

Notebook instructions let you define response preferences that should apply throughout the notebook.

### Steps

1. Open the notebook's **More options** menu.
2. Select **Instructions**.
   - In OneNote, look for **Copilot instructions** near the notebook name.
3. Enter:

   ```text
   Write for a project manager who is new to the initiative. Use plain language, short sections, and concise tables. Separate confirmed facts from assumptions and open questions. Never invent a date, owner, budget, or metric that is not present in the references.
   ```

4. Save the instructions.
5. Re-run this shorter prompt:

   ```text
   Give me a launch-readiness assessment.
   ```

### Compare

Did the result now:

- Use a clearer project-management structure?
- Separate facts from open questions?
- Avoid unsupported specifics?
- Reflect the intended audience and tone?

### What you learned

Use **notebook instructions** for durable behavior such as audience, tone, formatting, terminology, and rules. Use the individual prompt for the task-specific request.

---

## 12:00–16:00 — Task 5: Create a useful deliverable

Paste:

```text
Create a project update titled "Northwind Trail Pilot — Readiness Update."

Include:
1. A two-sentence executive summary.
2. A table of confirmed scope, target users, timing, and success measures.
3. The top three customer needs, with supporting evidence.
4. A Risks and Open Questions table with columns Item, Why it matters, Evidence available, and Next action.
5. Three decisions the team should make next.

Use only this notebook's references. Label any unsupported information as "Not found in references."
```

### If your experience offers Pages

Move the response into a Copilot Page or ask Copilot to create a page. Give the page the same title. Pages are useful when the result should become an editable, persistent, collaborative artifact.

### If Pages is not available

Keep the generated response in the notebook chat and continue. The learning goal is to create a structured output grounded in the notebook.

### Check your work

Your update should contain all five requested sections and clearly expose information gaps instead of hiding them.

---

## 16:00–18:00 — Task 6: Explore advanced notebook experiences

Complete one available option and review the others.

### Option A — Overview page in OneNote

Open the notebook in OneNote. Review the automatically generated **Overview** page. If you changed the references, refresh the overview so it reflects the current content.

### Option B — Audio overview

If **Audio overview** is available:

1. Generate an audio overview from the notebook.
2. Review the available format, voice, style, or duration controls.
3. Start playback long enough to confirm that it summarizes notebook content.

Audio generation may take longer than the lab window and may be subject to availability or usage limits.

### Option C — Mind map

If **Mind map** is available in Copilot Notebooks in OneNote:

1. Generate a mind map.
2. Expand a node.
3. Select a topic and ask Copilot to explain it.

Mind maps are useful for seeing relationships among themes. They may be private to the creator, available only on particular platforms, and retained for a limited period.

### Option D — Capture

If **Capture** is available, inspect the entry point but do not record anyone during this lab. Capture can bring in-person or some non-Teams conversations, whiteboard photos, and typed notes into a notebook. Always obtain consent and follow organizational policy before recording.

---

## 18:00–20:00 — Task 7: Share safely and finish

### Sharing inspection

1. Select **Share**.
2. Review the invite experience, but do not send an invitation unless you have an approved lab partner.
3. Before sharing, answer:
   - Do I have permission to share every referenced file?
   - Could sharing the notebook grant or request access to linked content?
   - Does the recipient have the license needed for premium reference types?
   - Is edit access appropriate?

### Reference cleanup

Practice the removal workflow:

1. Hover over `customer-feedback.md`.
2. Open its **More** menu.
3. Locate **Remove**.
4. Cancel unless you want to test the effect.

Removing a reference from a notebook does not delete the original file.

### Final knowledge check

Without looking back, complete these statements:

1. A Copilot Notebook is a scoped workspace grounded in __________.
2. To guarantee that an important file is considered, I should __________.
3. Notebook instructions are best for durable preferences such as __________.
4. Before sharing, I must check __________.
5. When a required fact is absent, Copilot should __________ rather than guess.

<details>
<summary>Suggested answers</summary>

1. The references selected for the notebook.
2. Add the file directly as a reference.
3. Audience, tone, structure, terminology, and response rules.
4. Permissions for the notebook and its linked references.
5. Identify the gap or label the information as not found.

</details>

---

# Feature map: what to explore after the lab

The 20-minute exercise teaches the core workflow. Use this map for continued learning.

| Capability | What it helps you do | Important note |
|---|---|---|
| References | Curate the content Copilot should use | Availability and source types vary by license |
| Grounded chat | Summarize, compare, analyze, and answer questions | Verify important claims against references |
| Custom instructions | Apply notebook-specific tone, format, focus, and rules | Shared members may be able to view or edit instructions |
| Copilot Pages | Turn responses into durable, editable content | Page functionality and creation options may vary |
| OneNote experience | Work in a fuller notebook-oriented interface | Some experiences are OneNote-only or rolling out |
| Overview page | Generate a high-level synthesis of references | Refresh it after changing references |
| Audio overview | Listen to a conversational or summarized review | License, language, platform, and daily limits may apply |
| Mind maps | Visualize themes and relationships | Platform, privacy, and retention constraints may apply |
| Capture | Bring live or offline moments into a notebook | Get consent and follow recording policy |
| Sharing | Collaborate around the notebook and references | Sharing may affect access to linked files |
| Reference removal | Narrow or refresh the notebook's scope | Removing a reference does not delete the source |

---

# Copilot Notebooks versus OneNote notebooks

| Use Copilot Notebooks when… | Use a traditional OneNote notebook when… |
|---|---|
| You have a defined project or question. | You need long-term, flexible note organization. |
| You want AI grounded in a curated set of references. | You want free-form notes, ink, drawings, tags, and manual hierarchy. |
| You need summaries, analysis, questions answered, or drafts from selected content. | You primarily need to capture and organize information yourself. |
| You want project-specific AI instructions and generated experiences. | You want a durable knowledge repository with conventional note management. |

They can be used together: Copilot Notebooks can appear inside OneNote while remaining a distinct AI-powered workspace.

---

# Current limits and design considerations

Keep these principles in mind:

1. **Licenses differ.** Copilot Chat and Microsoft Copilot users can see different reference types, limits, and generated features.
2. **Grounding has limits.** Large notebooks may contain more references than Copilot uses for a single grounded response. Add critical files directly and keep the notebook focused.
3. **Public links must be accessible.** Authenticated or paywalled web content may not work as a web reference.
4. **Permissions still apply.** Copilot uses content the user is allowed to access.
5. **Sharing is not read-only by default.** Review current collaboration permissions before inviting others.
6. **Chats can remain private.** A shared notebook does not necessarily expose each participant's Copilot conversation.
7. **Feature rollout varies.** The interface and available generated experiences may differ across accounts and platforms.
8. **Deletion can be consequential.** Confirm the current recovery behavior before deleting a notebook or generated item.
9. **AI can be wrong.** Validate important outputs before decisions or external use.

---

# Troubleshooting

## I cannot find Notebooks

- Confirm that you are signed in with the intended account.
- Check the Microsoft Copilot app's left navigation and app launcher.
- Confirm your license and SharePoint or OneDrive service eligibility.
- Ask your administrator whether organizational policy restricts the feature.

## I cannot add a source

- Confirm the source type is supported for your license.
- Confirm you have permission to the file or location.
- For web links, confirm the page is public and does not require authentication.
- Try adding a specific file rather than a broad location.
- If upload fails, use a smaller or less complex supported file.

## The response is generic

- Add more relevant references.
- Remove unrelated references.
- Name the exact files or subjects in the prompt.
- Specify the output fields and format.
- Tell Copilot not to infer missing information.
- Add notebook instructions for durable expectations.

## A collaborator cannot use a reference

- Confirm the collaborator has access to the linked file.
- Confirm you are allowed to grant access.
- Check whether the reference is a premium source that requires a different license.
- Share the containing OneNote notebook when a OneNote page or section requires it.

## I do not see an advanced feature

The feature may depend on license, organization policy, platform, language, region, or staged rollout. Complete the core lab without it and review the official documentation for current availability.

---

# Challenge exercises

Use these after the timed lab.

## Challenge 1 — Test the grounding boundary

Ask a question whose answer does not appear in either reference:

```text
What is the approved budget for this pilot?
```

A good response should state that the budget is not available in the references.

## Challenge 2 — Change the evidence set

Temporarily remove `customer-feedback.md`, then ask:

```text
What are the top customer concerns?
```

Compare the result with the earlier answer. Re-add the reference afterward.

## Challenge 3 — Create an executive version

Change the notebook instructions to:

```text
Write for an executive audience. Lead with the decision required, limit responses to 150 words unless asked otherwise, and highlight risks in a table.
```

Re-run the launch-readiness prompt and compare the output.

## Challenge 4 — Build a reusable prompt

Adapt this template to your own project:

```text
Using only this notebook, create a [deliverable] for [audience].
Include [required sections].
Use [format and length].
Distinguish confirmed facts, assumptions, conflicts, and missing information.
For each recommendation, explain which references support it.
```

---

# Instructor or facilitator notes

## Suggested pacing

| Time | Activity |
|---:|---|
| 2 minutes | Create the notebook and explain the scoped-workspace model |
| 3 minutes | Add references and explain the grounding boundary |
| 4 minutes | Run grounded prompts and inspect evidence |
| 3 minutes | Add notebook instructions and compare results |
| 4 minutes | Generate a structured project update |
| 2 minutes | Explore one advanced feature |
| 2 minutes | Review sharing, cleanup, and knowledge check |

## Success criteria

A learner has completed the lab when they can show:

- A notebook named `Northwind Trail Launch Lab`
- Two sample references
- At least one grounded summary
- At least one gaps-or-conflicts analysis
- Saved notebook instructions
- A structured project update
- An explanation of the sharing risk for linked files

## Facilitation tips

- Emphasize the **reference boundary** more than prompt cleverness.
- Ask learners to inspect evidence instead of trusting polished prose.
- Celebrate “not found” as a correct answer when the references lack a fact.
- Avoid spending the timed lab waiting for optional generated features.
- If the UI differs, teach the intended action rather than the exact button position.

---

# Official Microsoft resources

- [Get started with Microsoft Copilot Notebooks](https://support.microsoft.com/en-gb/microsoft-365-copilot/get-started-with-microsoft-365-copilot-notebooks)
- [How Microsoft Copilot Notebooks works](https://support.microsoft.com/en-us/microsoft-365-copilot/how-microsoft-365-copilot-notebooks-works)
- [Add references to a Copilot Notebook](https://support.microsoft.com/en-us/microsoft-365-copilot/add-references-to-your-microsoft-365-copilot-notebook)
- [Get answers and insights about a notebook](https://support.microsoft.com/en-us/microsoft-365-copilot/get-answers-and-insights-about-your-microsoft-365-copilot-notebook)
- [Provide custom instructions](https://support.microsoft.com/en-us/microsoft-365-copilot/provide-custom-instructions-for-your-microsoft-365-copilot-notebook)
- [Share a Copilot Notebook](https://support.microsoft.com/en-us/microsoft-365-copilot/share-a-microsoft-365-copilot-notebook)
- [Frequently asked questions](https://support.microsoft.com/en-us/microsoft-365-copilot/frequently-asked-questions-about-microsoft-365-copilot-notebooks)
- [Copilot Notebooks licensing](https://support.microsoft.com/en-us/microsoft-365-copilot/copilot-notebooks-licensing)
- [Audio overviews](https://support.microsoft.com/en-us/microsoft-365-copilot/get-an-audio-overview-of-your-microsoft-365-copilot-notebook)
- [Mind maps](https://support.microsoft.com/en-us/microsoft-365-copilot/mindmap-copilot-notebooks)
- [Overview page](https://support.microsoft.com/en-us/microsoft-365-copilot/view-an-overview-page-in-microsoft-365-copilot-notebooks)
- [Capture conversations and ideas](https://support.microsoft.com/en-us/microsoft-365-copilot/capture-conversations-copilot-notebooks)

---

## Repository structure

```text
copilot-notebooks-lab/
├── README.md
├── lab-files/
│   ├── customer-feedback.md
│   └── project-brief.md
└── LICENSE
```

## License

This lab is provided under the MIT License. See [`LICENSE`](LICENSE).

