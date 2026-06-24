# 4-Year Project Plan Creation Workflow

**Purpose:** Standardized workflow for creating T-Shaped 4-Year Project Plans for ANY engineering branch (or other domains).

**Target Audience:** Students who have chosen their branch and want strategic guidance on how to succeed in it.

**Output Format:**
- **Markdown document** → `FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md`
- **PDF version (optional)** → `FourYearProjectPlan/T-Shaped-Plan-[BRANCH].pdf`
- **Status tracking** → `.txt` files for resume capability after `/clear`

**Why This Matters:** Slide decks and videos tell students *what* the branch is. The 4-year plan tells them *how* to succeed in it. Together, they form a complete educational resource.

---

## Initial Step: Branch Selection

**When you read this file, you MUST ask the user:**

> "Which branch would you like to create a 4-year plan for?
> 
> **Note:** Make sure the following already exist for this branch:
> - ✅ HTML slide deck (`slides/[BRANCH].html`)
> - ✅ Markdown documentation (`docs/[BRANCH].md`)
> - ✅ Research file (`resources/[BRANCH]_syllabus.md`)
> 
> If these don't exist, complete the slide deck workflow first (see `generic_task.md`)."

---

## Workflow Steps

### **Step 0: Prerequisites Check**

**CRITICAL:** Before starting, verify these files exist:

```bash
# Check if branch slide deck exists
ls -la slides/[BRANCH].html
ls -la docs/[BRANCH].md
ls -la resources/[BRANCH]_syllabus.md
```

**If any file is missing:**
- STOP this workflow
- Complete the slide deck workflow first (`generic_task.md`)
- Return here once all three files exist

**If all files exist, proceed to Step 1.**

---

### **Step 1: Gather Existing Materials**

**Objective:** Collect all existing branch information as source material

**Estimated Time:** 15-30 minutes

**Source Materials (in order of importance):**

1. **Branch Research File** (`resources/[BRANCH]_syllabus.md`)
   - Complete curriculum breakdown (year-wise/semester-wise)
   - Career paths and salary ranges
   - Skills required
   - Industry trends and AI impact
   - Pros and cons
   - This is your PRIMARY source

2. **Branch Markdown Documentation** (`docs/[BRANCH].md`)
   - 20 slides of comprehensive content
   - Speaker notes with detailed explanations
   - Real-world projects section
   - Educational resources section
   - Decision framework

3. **Branch HTML Slide Deck** (`slides/[BRANCH].html`)
   - Visual presentation of key points
   - May have additional context in speaker notes

4. **Template Reference** (`FourYearProjectPlan/T-Shaped-Plan-Robotics-AI.md`)
   - Example of completed 4-year plan
   - Writing style and tone reference
   - Structure and flow model

**Actions:**
1. Read `resources/[BRANCH]_syllabus.md` completely
2. Read `docs/[BRANCH].md` for additional context
3. Review the Robotics example for writing style
4. Take notes on key specializations/verticals you identify

**Status Update:**
```
Create: status/4year_[BRANCH]_status.txt
---
Step 1: Material Gathering - COMPLETED
Source files reviewed:
- resources/[BRANCH]_syllabus.md
- docs/[BRANCH].md
- slides/[BRANCH].html
Next step: Identify verticals
Date: [timestamp]
---
```

---

### **Step 2: Identify Specialization Verticals**

**Objective:** Define 5-6 distinct, realistic specialization paths within the branch

**Estimated Time:** 30-45 minutes

**Source Priority:**
1. Career paths section in `resources/[BRANCH]_syllabus.md`
2. Industry sectors from slide deck
3. Job descriptions and hiring trends
4. Elective subjects mentioned in curriculum

**Vertical Selection Criteria:**

A good vertical MUST be:
- ✅ **Distinct** - Clearly different from other verticals (not overlapping)
- ✅ **Hirable** - Companies actually recruit for this specifically
- ✅ **Achievable** - Students can build depth in 2-3 years
- ✅ **Specific** - More specific than the branch name itself
- ❌ **NOT generic** - "Software Development" is not a vertical; "Backend Systems" is
- ❌ **NOT too narrow** - "React Development" is a tool, not a vertical

**How to Find Verticals:**

1. **From Curriculum Analysis:**
   - Look at elective clusters (3-4 electives in same area = potential vertical)
   - Identify major subjects (e.g., Power Systems, Control Systems in EE)
   - Notice lab sequences (signal processing labs, VLSI labs = verticals)

2. **From Career Paths:**
   - Entry-level job roles mentioned (Backend Engineer, VLSI Design Engineer)
   - Mid-level specializations (Solutions Architect, Control Systems Engineer)
   - Industry sectors (Cloud Infrastructure, Embedded Systems, Data Engineering)

3. **From Industry Trends:**
   - Hot hiring areas (AI/ML, Cloud, Cybersecurity)
   - Emerging technologies specific to branch
   - Research areas with industry applications

**Target: 5-6 Verticals**

Create a table like this:

| Vertical Name | What it actually means | Where it shows up |
|---|---|---|
| [Vertical 1] | [Technical work description] | [Industries/companies] |
| [Vertical 2] | [Technical work description] | [Industries/companies] |
| ... | ... | ... |

**Example - Computer Science:**
- Backend Systems & Distributed Computing
- Frontend & User Experience Engineering  
- Data Engineering & Analytics
- Machine Learning & AI Systems
- DevOps & Cloud Infrastructure
- Security & Privacy Engineering

**Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
Step 2: Vertical Identification - COMPLETED
Verticals identified: [count]
Verticals:
1. [Vertical 1 name]
2. [Vertical 2 name]
...
Next step: Draft 4-year plan
Date: [timestamp]
---
```

**Approval Gate:**
- Present identified verticals to user
- Explain why each was chosen
- Wait for explicit approval before proceeding
- ❌ DO NOT proceed to Step 3 without approval

---

### **Step 3: Draft the 4-Year Plan**

**Objective:** Fill the template with branch-specific content

**Estimated Time:** 2-3 hours

**Template Location:** `docs/4year_plan_template.md`

**Process:**

1. **Copy Template:**
   ```bash
   cp docs/4year_plan_template.md FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
   ```

2. **Work Through Placeholders Systematically:**

   Go section by section, replacing placeholders with content from your source materials.

   **Section 1: Introduction (Why This Document Exists)**
   - `[BRANCH_NAME]` → Use full name
   - `[DESCRIBE_BRANCH_APPEAL]` → From slide 2 (Overview) + research file intro
   - `[DESCRIBE_BRANCH_CHALLENGE]` → Think about structural challenges (too broad? too theoretical? interdisciplinary confusion?)
   - `[EXPLAIN_SPECIFIC_RISK]` → Create a concrete, visceral example

   **Section 2: T-Shaped Model**
   - `[LIST_BREADTH_AREAS]` → From curriculum overview (first 2 years typically)
   - Keep the T-shaped explanation consistent (don't need to customize much)

   **Section 3: Choosing Your Vertical**
   - Use your 5-6 verticals from Step 2
   - Fill the table completely
   - Make descriptions specific and technical

   **Section 4: Year-by-Year Plan**
   
   *Year 1:*
   - `[LIST_YEAR_1_FOUNDATIONS]` → From Year 1-2 curriculum in research file
   - `[SUGGEST_STARTER_PROJECTS]` → From "Real-World Projects" slide or research file
   
   *Year 2:*
   - `[ELECTIVE_EXAMPLE]` → Use actual elective names from curriculum if available
   - `[MATH_EXAMPLES]` → Match math to verticals (e.g., "linear algebra for ML, differential equations for control")
   
   *Year 3:*
   - `[READING_MATERIALS]` → Based on branch (research papers? industry blogs? standards?)
   - `[BREADTH_INTEGRATION]` → How does specialization connect to the broader branch?
   
   *Year 4:*
   - `[CAPSTONE_GUIDANCE]` → Branch-specific advice on final year projects
   - `[TOOLS_LIBS_COMPONENTS]` → What's okay to use vs. what to build

   **Section 5: Post-Graduation Paths**
   - `[LIST_HOT_VERTICALS]` → Pick 2-3 verticals from your table with strong hiring
   - `[INDIAN_INDUSTRY_CONTEXT]` → From "Career Opportunities" slides + salary data
   - `[KEY_RECRUITERS]` → From research file (ISRO, TCS, startups, etc.)
   - `[RESEARCH_VERTICALS]` → Which verticals benefit from M.Tech?
   - `[MTECH_EXAMPLE]` → Give concrete M.Tech specialization examples

   **Section 6: Honest Reminders**
   - `[TIMELESS_FUNDAMENTALS]` → Core topics that won't change (math, physics, core subjects)
   - `[FUTURE_YEAR]` → Use graduation year + 5

   **Section 7: Branch-Specific Resources (Optional)**
   - Use "Educational Resources" slide content
   - Add competitions from research file
   - Include professional bodies (IEEE, ACM, etc.)

3. **Remove Template Instructions:**
   - Delete everything after "This document is meant to be revisited..."
   - Remove all instruction sections
   - Final document should be clean, student-facing content only

**Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
Step 3: 4-Year Plan Drafting - COMPLETED
File: FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
Word count: ~[X] words
All placeholders filled: YES
Template instructions removed: YES
Next step: Quality review
Date: [timestamp]
---
```

**Approval Gate:**
- Inform user that draft is complete
- Share file location and word count
- Wait for explicit approval before proceeding
- ❌ DO NOT proceed to Step 4 without approval

---

### **Step 4: Quality Review & Refinement**

**Objective:** Ensure the plan meets quality standards

**Estimated Time:** 30-45 minutes

**Quality Checklist:**

**Content Quality:**
- [ ] All `[PLACEHOLDERS]` replaced with actual content
- [ ] 5-6 distinct, realistic verticals defined
- [ ] Verticals are specific and hirable (not generic)
- [ ] Year-by-year plans have concrete, actionable advice
- [ ] Examples use real course names, company names, tools
- [ ] Indian industry context included with specific details
- [ ] Post-graduation paths are realistic and specific
- [ ] Math/fundamentals emphasized appropriately

**Writing Quality:**
- [ ] Tone is direct and honest (no marketing speak)
- [ ] Second person ("you") used throughout
- [ ] Examples are concrete, not vague
- [ ] No hand-holding or condescension
- [ ] Hard truths acknowledged (not sugar-coated)
- [ ] Specific enough to be useful, not generic platitudes

**Structure Quality:**
- [ ] All sections present and complete
- [ ] Logical flow from section to section
- [ ] Year 1-4 progression makes sense
- [ ] Verticals mentioned consistently throughout
- [ ] No repetition or redundancy

**Technical Quality:**
- [ ] Length: 3,000-4,500 words (10-15 KB)
- [ ] Template instructions completely removed
- [ ] No formatting errors
- [ ] Markdown renders correctly
- [ ] No typos or grammatical errors

**Common Issues to Fix:**

❌ **Generic advice** → ✅ **Specific advice**
- "Work hard" → "Choose internships with 3+ months on one problem under one mentor"

❌ **Too many verticals** → ✅ **Right number**
- 10 verticals (overwhelming) → 5-6 verticals (actionable)

❌ **Overlapping verticals** → ✅ **Distinct verticals**
- "Web Dev" + "Full Stack" → "Frontend" + "Backend Systems"

❌ **Marketing tone** → ✅ **Honest tone**
- "Best branch ever!" → "This branch has specific risks..."

**Actions:**
1. Read through the entire document as if you're a student
2. Check every item on the quality checklist
3. Fix any issues found
4. Verify word count is in target range (3,000-4,500)

**Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
Step 4: Quality Review - COMPLETED
Quality checklist: All items passed
Issues fixed: [count]
Final word count: ~[X] words
Next step: Commit to repository
Date: [timestamp]
---
```

---

### **Step 5: Additional Research (If Needed)**

**Objective:** Fill any gaps that existing materials don't cover

**When to do this:** Only if you cannot find sufficient information in existing files

**Estimated Time:** 30-60 minutes (if needed)

**Common Gaps:**

1. **M.Tech Specializations:**
   - Search: "[BRANCH] M.Tech specializations IIT NIT 2026"
   - Look for specific program names (not generic)

2. **Professional Bodies:**
   - Search: "[BRANCH] professional associations India"
   - Search: "[BRANCH] IEEE society" or "ACM SIG"

3. **Competitions:**
   - Search: "[BRANCH] competitions students India 2026"
   - Search: "[BRANCH] hackathons challenges"

4. **Elective Course Names:**
   - Search: "IIT [Top IIT] [BRANCH] electives syllabus"
   - Look for actual course names to use in examples

5. **Industry Certifications:**
   - Search: "[BRANCH] certifications professionals"
   - Look for recognized credentials in the field

**Search Strategy:**
- Use WebSearch for quick lookups
- Use WebFetch for specific university pages or professional body sites
- Don't spend more than 60 minutes on additional research
- Most content should already be in existing files

**Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
Step 5: Additional Research - COMPLETED (if performed)
Additional sources: [count]
Gaps filled: [list]
Next step: Final review
Date: [timestamp]
---
```

---

### **Step 6: Commit and Push**

**Objective:** Save the 4-year plan to repository

**Estimated Time:** 5 minutes

**Actions:**
```bash
git add FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
git add status/4year_[BRANCH]_status.txt
git commit -m "Add [BRANCH_NAME] 4-Year T-Shaped Project Plan"
git push
```

**Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
Step 6: Commit - COMPLETED
Committed: FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
Repository: Updated
Next step: Generate PDF (optional)
Date: [timestamp]
---
```

---

### **Step 7: Generate PDF (Optional)**

**Objective:** Create PDF version for offline distribution

**Estimated Time:** 5-10 minutes

**Using Pandoc (if available):**
```bash
pandoc FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md \
  -o FourYearProjectPlan/T-Shaped-Plan-[BRANCH].pdf \
  --pdf-engine=xelatex \
  -V geometry:margin=1in \
  -V fontsize=11pt
```

**Alternative Methods:**
- Use online Markdown to PDF converters
- Use VS Code Markdown PDF extension
- Use Google Docs (import markdown, export PDF)

**If PDF Generation Succeeds:**
```bash
git add FourYearProjectPlan/T-Shaped-Plan-[BRANCH].pdf
git commit -m "Add PDF version of [BRANCH_NAME] 4-Year Plan"
git push
```

**Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
Step 7: PDF Generation - COMPLETED (if performed)
PDF file: FourYearProjectPlan/T-Shaped-Plan-[BRANCH].pdf
File size: ~[X] KB
Next step: Final validation
Date: [timestamp]
---
```

---

### **Step 8: Final Validation & Completion**

**Objective:** Verify everything is complete and mark as done

**Validation Tasks:**
1. ✅ Markdown file committed and pushed
2. ✅ PDF generated (if applicable)
3. ✅ All quality checks passed
4. ✅ No placeholders remaining
5. ✅ File naming convention followed
6. ✅ Document renders correctly on GitHub
7. ✅ Length is appropriate (3,000-4,500 words)
8. ✅ Writing style matches reference example

**Final Status Update:**
```
Update: status/4year_[BRANCH]_status.txt
---
✅ PROJECT COMPLETE - [BRANCH_NAME] 4-Year Plan

Deliverables:
- 4-Year Plan: FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
- PDF Version: FourYearProjectPlan/T-Shaped-Plan-[BRANCH].pdf (if generated)

Statistics:
- Word count: ~[X] words
- Verticals defined: [X]
- Completion date: [timestamp]

Related Resources:
- Slide Deck: slides/[BRANCH].html
- Documentation: docs/[BRANCH].md
- Research: resources/[BRANCH]_syllabus.md
- Video: [YouTube URL if available]

Status: COMPLETED ✅
---
```

**Update Task Tracker:**
- Add to completed list in `engg_task.md` (or domain-specific tracker)
- Update counts and statistics
- Document any lessons learned

---

## Status File Format

**File:** `status/4year_[BRANCH]_status.txt`

**Purpose:** Track progress, enable resume after `/clear`, provide quick reference

**Note:** Status files are `.txt` and gitignored (stay local, not committed to repository)

**Template:**
```
========================================
4-YEAR PLAN STATUS: [BRANCH_NAME]
========================================

Branch Details:
- Full Name: [BRANCH_NAME]
- Abbreviation: [BRANCH]
- Domain: Engineering/Commerce/Arts/Science
- Started: [date]
- Status: IN_PROGRESS / COMPLETED

----------------------------------------
PROGRESS TRACKER
----------------------------------------

[✅/⏳/❌] Step 1: Material Gathering
   Files reviewed: [count]
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 2: Vertical Identification
   Verticals: [count]
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 3: Plan Drafting
   File: FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
   Word count: [X]
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 4: Quality Review
   Quality checks passed: [X]/[Total]
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 5: Additional Research
   Additional sources: [count]
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 6: Commit
   Committed: YES/NO
   Date: [timestamp]

[✅/⏳/❌] Step 7: PDF Generation
   PDF created: YES/NO
   Date: [timestamp]

[✅/⏳/❌] Step 8: Final Validation
   All checks passed: YES/NO
   Date: [timestamp]

----------------------------------------
VERTICALS IDENTIFIED
----------------------------------------
1. [Vertical 1 name] - [Brief description]
2. [Vertical 2 name] - [Brief description]
...

----------------------------------------
NEXT STEPS
----------------------------------------
Current Step: [Step number and name]
Action Required: [What needs to be done next]
Waiting On: User Approval / Drafting / Review / Other
Notes: [Any relevant notes or blockers]

----------------------------------------
FILES CREATED
----------------------------------------
- [ ] FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md
- [ ] FourYearProjectPlan/T-Shaped-Plan-[BRANCH].pdf
- [✅] status/4year_[BRANCH]_status.txt

========================================
Last Updated: [timestamp]
========================================
```

---

## Resume Workflow After `/clear`

**When resuming work on a 4-year plan after `/clear`:**

1. Read `status/4year_[BRANCH]_status.txt`
2. Identify current step and completion status
3. Continue from the next incomplete step
4. Do NOT repeat completed steps
5. Update status file as you progress

**Example:**
```
User: Continue working on CSE 4-year plan
Assistant: [Reads status/4year_CSE_status.txt]
          [Sees Step 3 is in progress]
          [Continues drafting from where it left off]
```

---

## Where to Search for Material

### **Primary Sources (MUST USE FIRST):**

1. **Branch Research File** (`resources/[BRANCH]_syllabus.md`)
   - ✅ Curriculum breakdown
   - ✅ Career paths
   - ✅ Salary data
   - ✅ Skills required
   - ✅ Industry trends
   - ✅ Pros/cons
   - **This contains 90% of what you need**

2. **Branch Markdown Docs** (`docs/[BRANCH].md`)
   - ✅ 20 slides of detailed content
   - ✅ Speaker notes (200-500 words each)
   - ✅ Real-world projects
   - ✅ Educational resources
   - ✅ Decision framework

3. **Branch Slide Deck** (`slides/[BRANCH].html`)
   - ✅ Visual summary
   - ✅ Additional speaker notes
   - ✅ Key highlights

### **Secondary Sources (IF NEEDED):**

Use WebSearch/WebFetch ONLY if primary sources lack specific information:

**For M.Tech Programs:**
- IIT/NIT department websites
- M.Tech specialization lists
- Search: "[BRANCH] M.Tech IIT specializations"

**For Professional Bodies:**
- IEEE societies
- ACM SIGs  
- Domain-specific associations
- Search: "[BRANCH] professional association India"

**For Competitions:**
- Hackathon lists
- Technical competitions
- Industry challenges
- Search: "[BRANCH] competitions students 2026"

**For Course Names:**
- IIT/NIT syllabi
- Department elective lists
- Search: "IIT [name] [BRANCH] electives"

### **What NOT to Search:**

❌ Don't search for generic "how to succeed" advice
❌ Don't search for basic branch overview (already in slides)
❌ Don't search for salary data (already in research file)
❌ Don't search for curriculum (already documented)
❌ Don't copy content from random blogs or websites

**Rule of Thumb:** If it's in the existing files (90% probability), use that. Only search for very specific gaps (M.Tech names, competition names, specific certifications).

---

## Integration with Existing Workflow

**Relationship to Slide Deck Workflow (`generic_task.md`):**

| Workflow | Output | Purpose | Prerequisite |
|----------|--------|---------|--------------|
| `generic_task.md` | Slides + Video + MD | What the branch is | None |
| `execution_generic_task.md` | 4-Year Plan | How to succeed in it | Slide deck complete |

**Recommended Order:**
1. Complete slide deck workflow first (7 steps)
2. Then create 4-year plan (8 steps)
3. Result: Complete educational package

**Complete Deliverables per Branch:**
1. ✅ HTML slide deck (`slides/[BRANCH].html`)
2. ✅ MP4 video (YouTube)
3. ✅ Markdown documentation (`docs/[BRANCH].md`)
4. ✅ Research compilation (`resources/[BRANCH]_syllabus.md`)
5. ✅ **NEW:** 4-Year T-Shaped Plan (`FourYearProjectPlan/T-Shaped-Plan-[BRANCH].md`)
6. ✅ **NEW:** PDF version (optional)

---

## Quality Standards

Every 4-year plan must meet these standards:

**Content Standards:**
- [ ] 5-6 distinct, hirable verticals
- [ ] Specific examples (course names, company names, tools)
- [ ] Actionable advice (not generic platitudes)
- [ ] Honest about risks and challenges
- [ ] Indian industry context included
- [ ] Real career paths and progression

**Writing Standards:**
- [ ] Direct, honest tone (no marketing)
- [ ] Second person throughout
- [ ] Concrete examples, not vague advice
- [ ] Hard truths acknowledged
- [ ] 3,000-4,500 words
- [ ] No template instructions remaining

**Technical Standards:**
- [ ] All placeholders filled
- [ ] Markdown renders correctly
- [ ] No typos or errors
- [ ] Proper formatting
- [ ] Clean file structure

**User Experience:**
- [ ] Easy to read and follow
- [ ] Clear progression (Year 1 → 4)
- [ ] Verticals well-defined
- [ ] Post-graduation paths realistic
- [ ] Resources helpful and current

---

## Repository Structure

```
project-root/
├── execution_generic_task.md   # This file - 4-year plan workflow
├── generic_task.md              # Slide deck workflow
├── engg_task.md                 # Engineering branches tracker
│
├── docs/
│   ├── 4year_plan_template.md  # Template for 4-year plans
│   ├── template.md              # Markdown slide template
│   ├── template.html            # HTML slide template
│   ├── [BRANCH].md              # Branch documentation
│   └── ...
│
├── FourYearProjectPlan/         # 4-year plans (output)
│   ├── T-Shaped-Plan-Robotics-AI.md  # Example (already done)
│   ├── T-Shaped-Plan-CSE.md           # To be created
│   ├── T-Shaped-Plan-EC.md            # To be created
│   └── ...
│
├── resources/                   # Research compilations
│   ├── [BRANCH]_syllabus.md
│   └── ...
│
├── slides/                      # HTML slide decks
│   ├── [BRANCH].html
│   └── ...
│
└── status/                      # Status tracking (gitignored)
    ├── 4year_[BRANCH]_status.txt
    └── ...
```

---

## Approval Gates Summary

**Gate 1 - After Step 2:** Vertical identification approval required
**Gate 2 - After Step 3:** Draft 4-year plan approval required
**Gates 4-8:** Automatic progression unless issues found

User can review and provide feedback at any gate. Never skip approval gates.

---

## Tips for Success

1. **Use Existing Materials:** 90% of content is already in research/docs files
2. **Be Specific:** Use real names (courses, companies, tools, certifications)
3. **Stay Honest:** Include hard truths, don't oversell the branch
4. **Focus on Verticals:** This is the most critical part - get it right
5. **Match the Tone:** Read the Robotics example to calibrate your writing style
6. **Keep it Actionable:** Every section should have concrete next steps
7. **Avoid Generic Advice:** "Work hard" is useless; "Choose 3-month single-mentor internships" is useful
8. **Update Status:** Keep status file current for easy resume after `/clear`

---

## Common Pitfalls to Avoid

❌ **Starting without prerequisites** → ✅ Verify slide deck exists first
❌ **Too many verticals (8-10)** → ✅ Focus on 5-6 realistic ones
❌ **Overlapping verticals** → ✅ Make each distinct and specific
❌ **Generic, vague advice** → ✅ Concrete examples and actions
❌ **Marketing tone** → ✅ Honest, direct mentorship tone
❌ **Copying template instructions** → ✅ Remove all template sections
❌ **Not using existing research** → ✅ Primary sources contain 90% of content
❌ **Making up content** → ✅ Base everything on documented research

---

**Last Updated:** June 24, 2026  
**Version:** 1.0  
**Applies To:** All domains - Engineering (primary), Commerce, Arts, Science  
**Companion Document:** `generic_task.md` (slide deck workflow)
