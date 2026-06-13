# Generic Branch/Stream Creation Workflow

**Purpose:** Standardized workflow for creating educational career guide slide decks for ANY branch/stream (Engineering, Commerce, Arts, Science, etc.)

**Target Audience:** Students choosing their career path (high school, college, career switchers)

**Output Format:** 
- Interactive HTML slide deck (20 slides)
- Markdown documentation
- Research resources compilation
- Status tracking for resume capability

---

## Initial Step: Branch Selection

**When you read this file, you MUST ask the user:**

> "Which branch/stream would you like to create next? Please provide:
> 1. **Branch Name** (e.g., Aerospace Engineering, Chartered Accountancy, Psychology, Data Science)
> 2. **Abbreviation** (e.g., AE, CA, PSY, DS)
> 3. **Domain** (Engineering / Commerce / Arts / Science / Professional / Other)
> 4. **Target Degree** (B.Tech / B.Com / BA / BSc / Professional Certification / Other)
> 5. **Color Preference** (Optional - suggest based on branch if not provided)"

---

## Workflow Steps

### **Step 0: Setup (First Time Only)**

**Ensure directory structure exists:**
```bash
mkdir -p plans status resources
```

**Note:** Status and plan files (`.txt`) are gitignored and stay local only. They're for tracking progress and resuming work after `/clear`.

---

### **Step 1: Create Implementation Plan**

**Objective:** Plan the research, content structure, and execution strategy

**Estimated Time:** 30-60 minutes

**Actions:**
1. Read existing templates:
   - `docs/template.md` for markdown structure
   - `docs/template.html` for HTML structure
   - For engineering branches: `engg_task.md` for branch inventory and colors
2. Create a branch-specific plan document: `plans/{BRANCH_ABBREVIATION}_plan.md`
3. Plan should include:
   - Research sources (institutions, industry websites, salary data)
   - Content outline (20 slides mapped to branch-specific topics)
   - Timeline estimate
   - Resource requirements
   - Unique considerations for this branch/domain

**Status Update:**
```
Create/Update: status/{BRANCH_ABBREVIATION}_status.txt
---
Step 1: Plan Creation - COMPLETED
Plan file: plans/{BRANCH_ABBREVIATION}_plan.md
Next step: Resource gathering
Date: [timestamp]
---
```

**Approval Gate:** 
- Present plan to user
- Wait for explicit approval before proceeding
- ❌ DO NOT proceed to Step 2 without approval

---

### **Step 2: Research & Resource Gathering**

**Objective:** Gather comprehensive, authoritative information about the branch/stream

**Estimated Time:** 1-2 hours (can be longer for specialized/emerging fields)

**Research Sources (adapt based on domain):**

#### For Engineering Branches:
- **Academic Curricula:**
  - IIT curricula (IIT Bombay, IIT Madras, IIT Kharagpur, IIT Delhi)
  - NIT syllabi (NIT Delhi, NIT Trichy, NIT Rourkela)
  - GATE syllabus for the specific branch
  - AICTE curriculum guidelines
  - Top international universities (MIT OCW, Stanford, Georgia Tech)
- **Professional Bodies:**
  - IEEE (electrical, computer, electronics)
  - ACM (computer science)
  - ASME (mechanical)
  - ASCE (civil)
  - AIChE (chemical)
- **Industry Trends:**
  - Recent tech news and publications
  - GitHub trending projects (for software-related branches)
  - Research papers (arXiv, IEEE Xplore, Google Scholar)
  - Industry reports and white papers

#### For Commerce Streams:
- **Academic Programs:**
  - University syllabi (Delhi University, Mumbai University, top B-schools)
  - NCERT commerce curriculum
- **Professional Bodies:**
  - ICAI (Chartered Accountancy)
  - ICWA/CMA (Cost & Management Accounting)
  - CFA Institute (Financial Analysis)
  - ACCA (International accounting)
  - Company Secretaries Institute
- **Industry Standards:**
  - Accounting standards (IndAS, IFRS, GAAP)
  - Professional certification paths
  - Career progression frameworks

#### For Arts/Humanities:
- **Academic Institutions:**
  - Top university curricula (JNU, DU, international unis)
  - Department-specific syllabi
- **Professional Associations:**
  - Subject-specific professional bodies
  - Research associations
  - Industry guilds and councils
- **Career Resources:**
  - Career pathways documentation
  - Industry standards and best practices

#### For Science Streams:
- **Academic Programs:**
  - University BSc/MSc programs
  - Research institution guidelines (TIFR, IISc, etc.)
- **Certifications:**
  - Professional certifications in the field
  - Laboratory certifications
  - Research methodologies

#### Universal Research (ALL domains):
- **Salary & Compensation:**
  - LinkedIn Salary Insights
  - Glassdoor company reviews and salaries
  - AmbitionBox (India-specific)
  - Payscale salary data
  - Naukri/Indeed salary reports
  
- **Career Paths & Opportunities:**
  - Job portals (Naukri, Indeed, LinkedIn Jobs)
  - LinkedIn job postings and career paths
  - Company career pages (specific to field)
  - Industry hiring trends reports
  
- **Industry Trends (2026):**
  - Recent news articles (Google News, TechCrunch, etc.)
  - Industry reports and market research
  - Research papers and publications
  - Conference proceedings
  - Technology blogs and forums
  
- **AI & Technology Impact:**
  - How AI/automation affects this specific field
  - Future skills and adaptation strategies
  - Emerging technologies in the domain
  - Digital transformation trends
  
- **Educational Resources:**
  - **YouTube Channels:** Subject-specific educational channels
  - **Online Courses:** Coursera, edX, Udemy, NPTEL
  - **Free Resources:** MIT OCW, Khan Academy
  - **Books:** Standard textbooks and recommended reading
  - **Communities:** Reddit, Discord, professional forums
  
- **Practical Work & Projects:**
  - Typical student projects (undergraduate level)
  - Industry project examples
  - Hackathons, competitions, challenges
  - Open-source contributions (if applicable)
  - Portfolio examples

**Search Query Examples:**
- "[Branch] IIT syllabus curriculum 2026"
- "[Branch] salary India ISRO/TCS/Infosys 2026" (adapt company names)
- "[Branch] career path entry to senior level"
- "[Branch] AI impact machine learning automation 2026"
- "[Branch] YouTube channels courses online learning NPTEL"
- "[Branch] student projects final year ideas"
- "[Branch] pros cons advantages disadvantages career 2026"

**Actions:**
1. Use WebSearch and WebFetch tools to gather information
2. Compile research into: `resources/{BRANCH_ABBREVIATION}_syllabus.md`
3. Include:
   - Complete curriculum/syllabus (year-wise or semester-wise)
   - Career paths and salary ranges (entry → mid → senior)
   - Required skills and tools
   - Industry trends (2026 and beyond)
   - AI/technology impact
   - Educational resources
   - Pros and cons
   - Decision framework
   - All source URLs (for citations)

**Status Update:**
```
Update: status/{BRANCH_ABBREVIATION}_status.txt
---
Step 2: Research & Resource Gathering - COMPLETED
Resource file: resources/{BRANCH_ABBREVIATION}_syllabus.md
Sources: [count] web sources consulted
Word count: ~[X] words
Next step: Commit resources
Date: [timestamp]
---
```

**Commit & Push:**
```bash
git add resources/{BRANCH_ABBREVIATION}_syllabus.md status/{BRANCH_ABBREVIATION}_status.txt
git commit -m "Add {BRANCH_NAME} research and syllabus compilation"
git push
```

---

### **Step 3: Create Markdown Documentation**

**Objective:** Create comprehensive 20-slide content in markdown format

**Estimated Time:** 2-3 hours (includes writing speaker notes)

**Actions:**
1. Copy template: `cp docs/template.md docs/{BRANCH_ABBREVIATION}.md`
2. Fill ALL 20 slides with content from research
3. Write speaker notes (200-500 words per slide)
4. Customize content for the specific domain:

**20-Slide Structure (Universal):**

1. **Title** - Branch name and tagline
2. **Overview** - What is this branch/stream?
3. **Curriculum - Foundation** (Years 1-2 or foundational courses)
4. **Curriculum - Core Specialization** (Years 3 or core courses)
5. **Curriculum - Advanced** (Year 4 or advanced topics/electives)
6. **Skills Development** - Technical, professional, domain-specific
7. **Career Opportunities - Entry Level** - Roles, responsibilities, salaries
8. **Career Growth - Mid to Senior** - Advancement paths
9. **Industry Sectors** - Where graduates work
10. **Higher Education** - Masters, PhD, certifications, specializations
11. **Day in the Life** - Realistic work scenarios
12. **Compensation Deep Dive** - India and international salaries
13. **Current Trends** - What's hot in the field (2026)
14. **AI Impact - Disruption** - How AI/automation affects this field
15. **AI Impact - Adaptation** - How to stay relevant, future skills
16. **Educational Resources** - YouTube, courses, books, communities
17. **Real-World Projects** - Student and professional examples
18. **Pros & Cons** - Honest assessment of the field
19. **Decision Checklist** - Self-assessment for students
20. **Closing** - Summary and next steps

**Domain-Specific Adaptations:**

*Engineering:* Focus on labs, projects, technical skills, tool proficiency
*Commerce:* Focus on certifications, exams, practical training, articling
*Arts:* Focus on research, critical thinking, communication, creative work
*Science:* Focus on research, lab work, analytical methods, field work

**Status Update:**
```
Update: status/{BRANCH_ABBREVIATION}_status.txt
---
Step 3: Markdown Documentation - COMPLETED
MD file: docs/{BRANCH_ABBREVIATION}.md
Slides: 20/20 complete
Speaker notes: All slides
Word count: ~[X] words
Next step: Review and approval
Date: [timestamp]
---
```

**Approval Gate:**
- Inform user that markdown is complete
- Share file location and stats
- Wait for explicit approval before proceeding
- ❌ DO NOT proceed to Step 4 without approval

---

### **Step 4: Commit Markdown Documentation**

**Objective:** Save markdown documentation to repository

**Actions:**
```bash
git add docs/{BRANCH_ABBREVIATION}.md status/{BRANCH_ABBREVIATION}_status.txt
git commit -m "Add {BRANCH_NAME} complete documentation (20 slides with speaker notes)"
git push
```

**Status Update:**
```
Update: status/{BRANCH_ABBREVIATION}_status.txt
---
Step 4: Markdown Commit - COMPLETED
Committed: docs/{BRANCH_ABBREVIATION}.md
Repository: Updated
Next step: Create HTML slide deck
Date: [timestamp]
---
```

---

### **Step 5: Create HTML Slide Deck**

**Objective:** Create interactive HTML slide deck with images and full functionality

**Estimated Time:** 1-2 hours (includes finding images and testing)

**🚨 CRITICAL RULE:** ⚠️ **ALWAYS use `docs/template.html` as starting point** (NEVER copy existing branch HTML files)

**WHY THIS MATTERS:** 
- Existing branch HTML files contain branch-specific content, colors, and placeholders
- Copying them leads to confusion, errors, incomplete replacements, wrong colors
- Templates are designed with proper placeholders for systematic replacement
- **CONSEQUENCE OF VIOLATION:** Broken HTML, missing content, navigation issues, wasted debugging time

**Actions:**

1. **Copy Template:**
   ```bash
   cp docs/template.html slides/{BRANCH_ABBREVIATION}.html
   ```

2. **Replace Placeholders:**
   - `[BRANCH_NAME]` → Full branch name
   - `[BRANCH_ABBREVIATION]` → Short form
   - `[BRANCH_TAGLINE]` → Engaging one-liner
   - `[PRIMARY_COLOR]` → Main color (hex)
   - `[SECONDARY_COLOR]` → Lighter shade
   - `[ACCENT]` → Darker shade
   - All content from markdown file
   - All speaker notes

3. **Find and Test Images (3 required):**
   - Search Unsplash for relevant images
   - Format: `https://images.unsplash.com/photo-[ID]?w=800&q=80`
   - Test each URL: `curl -I "[URL]"` must return HTTP 200
   - Add to slides (typically slides 2, 3, 4)
   - Include alt text and photographer credit

4. **Color Scheme Selection:**

   **Engineering Branches:**
   - Computer/IT: Blues (#0066CC, #0EA5E9)
   - Electronics: Orange (#FF6600)
   - Electrical: Gold (#FFB800)
   - Mechanical: Gray/Silver (#64748B)
   - Civil: Terra Cotta (#DC582A)
   - Chemical: Green (#16A34A)
   - Aerospace: Sky Blue (#0369A1)
   - Biotech: Teal (#0D9488)

   **Commerce Streams:**
   - Accounting/CA: Dark Green (#047857)
   - Finance/CFA: Gold (#CA8A04)
   - Marketing: Red (#DC2626)
   - Management: Blue (#1E40AF)

   **Arts/Humanities:**
   - Psychology: Purple (#9333EA)
   - Literature: Burgundy (#991B1B)
   - History: Brown (#78350F)
   - Sociology: Teal (#0F766E)

   **Science Streams:**
   - Physics: Blue (#1D4ED8)
   - Chemistry: Green (#15803D)
   - Biology: Lime (#65A30D)
   - Mathematics: Purple (#7C3AED)

5. **Validation Checklist:**
   - [ ] All 20 slides present (`data-slide-number` = 20)
   - [ ] All 20 speaker notes sections filled
   - [ ] No `[PLACEHOLDER]` text remaining
   - [ ] Color variables set
   - [ ] 3 images loaded and tested
   - [ ] All slide content from markdown transferred
   - [ ] Navigation works (can test after commit)

**Status Update:**
```
Update: status/{BRANCH_ABBREVIATION}_status.txt
---
Step 5: HTML Slide Deck Creation - COMPLETED
HTML file: slides/{BRANCH_ABBREVIATION}.html
Slides: 20/20
Images: 3/3 (tested and working)
Colors: [PRIMARY_COLOR]
File size: ~[X]KB
Next step: Commit and push
Date: [timestamp]
---
```

---

### **Step 6: Commit and Push HTML Slide Deck**

**Objective:** Save HTML slide deck to repository and deploy to GitHub Pages

**Estimated Time:** 5-10 minutes (plus 1-2 minutes for GitHub Pages rebuild)

**Actions:**
```bash
git add slides/{BRANCH_ABBREVIATION}.html status/{BRANCH_ABBREVIATION}_status.txt
git commit -m "Add {BRANCH_NAME} HTML slide deck (20 slides)"
git push
```

**Post-Deployment Verification:**
1. Wait 1-2 minutes for GitHub Pages rebuild
2. Open URL in browser: `https://{GITHUB_USERNAME}.github.io/{REPOSITORY_NAME}/slides/{BRANCH_ABBREVIATION}.html`
   - **Engineering branches:** `https://tarakbluru.github.io/engineering-branch-slides/slides/{BRANCH_ABBREVIATION}.html`
   - Adapt repository name based on your domain/project
3. **Test Navigation:**
   - Arrow keys (left/right, up/down)
   - Spacebar (forward)
   - Click next/previous buttons
   - Touch/swipe (mobile)
   - Progress bar updates correctly
4. **Test Speaker Notes:**
   - Press 'N' key to toggle notes panel
   - Verify notes display for all 20 slides
   - Check notes panel can be closed
5. **Test Images:**
   - All 3 images load correctly
   - Alt text displays on hover
   - Photographer credits visible
6. **Test Mobile Responsiveness:**
   - Open browser dev tools (F12)
   - Switch to mobile view (Ctrl+Shift+M / Cmd+Shift+M)
   - Test on different screen sizes (phone, tablet)
   - Verify text readable and images scale properly
7. **Final Checks:**
   - No [PLACEHOLDER] text visible
   - Colors match branch theme
   - All content renders correctly
   - No console errors (check browser console)

**Status Update:**
```
Update: status/{BRANCH_ABBREVIATION}_status.txt
---
Step 6: HTML Commit & Deployment - COMPLETED
Committed: slides/{BRANCH_ABBREVIATION}.html
Repository: Updated
GitHub Pages: Deployed
URL: https://{GITHUB_USERNAME}.github.io/{REPOSITORY_NAME}/slides/{BRANCH_ABBREVIATION}.html
Next step: Final validation
Date: [timestamp]
---
```

---

### **Step 7: Final Validation & Completion**

**Objective:** Verify everything works and mark as complete

**Validation Tasks:**
1. ✅ All files committed and pushed
2. ✅ GitHub Pages deployment successful
3. ✅ HTML slides accessible via URL
4. ✅ Navigation functional
5. ✅ Images display correctly
6. ✅ Speaker notes accessible
7. ✅ Content accurate and complete
8. ✅ No broken links or placeholders

**Final Status Update:**
```
Update: status/{BRANCH_ABBREVIATION}_status.txt
---
✅ PROJECT COMPLETE - {BRANCH_NAME}

Deliverables:
- Research: resources/{BRANCH_ABBREVIATION}_syllabus.md
- Documentation: docs/{BRANCH_ABBREVIATION}.md
- Slide Deck: slides/{BRANCH_ABBREVIATION}.html
- Live URL: https://{GITHUB_USERNAME}.github.io/{REPOSITORY_NAME}/slides/{BRANCH_ABBREVIATION}.html

Statistics:
- Total slides: 20
- Total word count: ~[X] words
- Images: 3
- Research sources: [X]
- Completion date: [timestamp]

Status: COMPLETED ✅
---
```

**Update Task Tracker:**
- **Engineering branches:** Add to completed list in `engg_task.md`
- **Other domains:** Update your domain-specific tracker
- Update counts and statistics
- Document any lessons learned

---

## Status File Format

**File:** `status/{BRANCH_ABBREVIATION}_status.txt`

**Purpose:** Track progress, enable resume after `/clear`, provide quick reference

**Note:** Status files are `.txt` and gitignored (stay local, not committed to repository)

**Template:**
```
========================================
BRANCH CREATION STATUS: {BRANCH_NAME}
========================================

Branch Details:
- Full Name: {BRANCH_NAME}
- Abbreviation: {BRANCH_ABBREVIATION}
- Domain: Engineering/Commerce/Arts/Science/Other
- Color Scheme: Primary [HEX], Secondary [HEX], Accent [HEX]
- Started: [date]
- Status: IN_PROGRESS / COMPLETED

----------------------------------------
PROGRESS TRACKER
----------------------------------------

[✅/⏳/❌] Step 1: Plan Creation
   File: plans/{BRANCH_ABBREVIATION}_plan.md
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 2: Research & Resources
   File: resources/{BRANCH_ABBREVIATION}_syllabus.md
   Sources: [count]
   Status: [details]
   Committed: YES/NO
   Date: [timestamp]

[✅/⏳/❌] Step 3: Markdown Documentation
   File: docs/{BRANCH_ABBREVIATION}.md
   Slides: [X]/20
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 4: Markdown Commit
   Committed: YES/NO
   Date: [timestamp]

[✅/⏳/❌] Step 5: HTML Slide Deck
   File: slides/{BRANCH_ABBREVIATION}.html
   Images: [X]/3
   Status: [details]
   Date: [timestamp]

[✅/⏳/❌] Step 6: HTML Commit & Deploy
   Committed: YES/NO
   Deployed: YES/NO
   URL: [GitHub Pages URL]
   Date: [timestamp]

[✅/⏳/❌] Step 7: Final Validation
   All checks passed: YES/NO
   Date: [timestamp]

----------------------------------------
NEXT STEPS
----------------------------------------
Current Step: [Step number and name]
Action Required: [What needs to be done next]
Waiting On: User Approval / Research / Commit / Other
Notes: [Any relevant notes or blockers]

----------------------------------------
FILES CREATED
----------------------------------------
- [ ] plans/{BRANCH_ABBREVIATION}_plan.md
- [ ] resources/{BRANCH_ABBREVIATION}_syllabus.md
- [ ] docs/{BRANCH_ABBREVIATION}.md
- [ ] slides/{BRANCH_ABBREVIATION}.html
- [✅] status/{BRANCH_ABBREVIATION}_status.txt

========================================
Last Updated: [timestamp]
========================================
```

---

## Resume Workflow After `/clear`

**When resuming work on a branch after `/clear`:**

1. Read `status/{BRANCH_ABBREVIATION}_status.txt`
2. Identify current step and completion status
3. Continue from the next incomplete step
4. Do NOT repeat completed steps
5. Update status file as you progress

**Example:**
```
User: Continue working on Aerospace Engineering
Assistant: [Reads status/AE_status.txt]
          [Sees Step 5 is in progress]
          [Continues creating HTML slide deck from where it left off]
```

---

## Domain-Specific Customizations

### Engineering Branches
- Focus on: Labs, projects, technical skills, software tools
- Curriculum: 4 years, 8 semesters
- Emphasis on: Hands-on work, internships, placement stats
- Key sections: Technical skills, industry tools, lab work

### Commerce Streams  
- Focus on: Certifications, exams, practical training, articleship
- Curriculum: Varies (3-year degree, 5-year CA, etc.)
- Emphasis on: Professional exams, networking, internships
- Key sections: Certification paths, exam strategy, career progression

### Arts/Humanities
- Focus on: Research, critical thinking, communication, creative work
- Curriculum: 3-4 years, varies by program
- Emphasis on: Writing, analysis, projects, field work
- Key sections: Research opportunities, career diversity, skill development

### Science Streams
- Focus on: Research, lab work, analytical methods, field work
- Curriculum: 3-4 years BSc, higher ed common
- Emphasis on: Research skills, lab experience, higher studies
- Key sections: Laboratory work, research projects, PhD paths

### Professional Certifications
- Focus on: Exam preparation, practical application, career transition
- Curriculum: Varies (6 months to 3 years)
- Emphasis on: Pass rates, study resources, ROI
- Key sections: Exam structure, preparation strategy, career impact

---

## Quality Standards

Every branch/stream deliverable must meet these standards:

**Content Quality:**
- [ ] Accurate, current information (2026 data)
- [ ] Real salary ranges (not generic estimates)
- [ ] Specific career paths (not vague descriptions)
- [ ] Honest pros and cons (not marketing)
- [ ] Practical examples (not theoretical only)

**Technical Quality:**
- [ ] All 20 slides complete
- [ ] Speaker notes 200-500 words each
- [ ] 3 working images with credits
- [ ] No placeholders remaining
- [ ] HTML parses cleanly
- [ ] Responsive design works

**User Experience:**
- [ ] Easy navigation
- [ ] Readable on mobile
- [ ] Accessible (ARIA, WCAG AA)
- [ ] Speaker notes toggle works
- [ ] Fast loading

**Documentation:**
- [ ] All sources cited
- [ ] Status file updated
- [ ] Clean commit messages
- [ ] README updated if needed

---

## Repository Structure

```
project-root/
├── generic_task.md              # This file - universal workflow
├── engg_task.md                 # Engineering branches tracker (domain-specific)
├── README.md                    # Project documentation
│
├── plans/                       # Implementation plans (*.md, not committed)
│   ├── AE_plan.md
│   ├── CA_plan.md
│   └── [BRANCH]_plan.md
│
├── resources/                   # Research compilations
│   ├── aerospace_engineering_syllabus.md
│   ├── chartered_accountancy_syllabus.md
│   └── [BRANCH]_syllabus.md
│
├── docs/                        # Markdown documentation
│   ├── template.md              # Markdown template
│   ├── template.html            # HTML template
│   ├── Aerospace.md
│   ├── CA.md
│   └── [BRANCH].md
│
├── slides/                      # HTML slide decks
│   ├── Aerospace.html
│   ├── CA.html
│   └── [BRANCH].html
│
└── status/                      # Status tracking files (*.txt, gitignored)
    ├── AE_status.txt
    ├── CA_status.txt
    └── [BRANCH]_status.txt
```

**Note:** `.txt` files (status and plans) are gitignored and stay local for progress tracking.

---

## Approval Gates Summary

**Gate 1 - After Step 1:** Plan approval required
**Gate 2 - After Step 3:** Markdown content approval required
**Gates 3-7:** Automatic progression unless issues found

User can review and provide feedback at any gate. Never skip approval gates.

---

## Tips for Success

1. **Be Thorough:** Research deeply, don't guess or use generic content
2. **Stay Current:** Use 2026 data, latest trends, current salaries
3. **Be Honest:** Include real pros and cons, don't oversell
4. **Test Everything:** URLs, images, navigation, mobile view
5. **Update Status:** Keep status file current for easy resume
6. **Commit Often:** After each major step, commit progress
7. **Domain Awareness:** Adapt content to domain (engineering vs commerce vs arts)
8. **User-Centric:** Write for high school/college students making career choices

---

**Last Updated:** June 13, 2026  
**Version:** 1.0  
**Applies To:** All domains - Engineering, Commerce, Arts, Science, Professional Certifications
