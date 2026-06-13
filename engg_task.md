# Engineering Branch Slide Decks - Project Tracker

## Project Overview
Create interactive HTML slide decks for engineering branches to help a high school student (daughter) evaluate career options.

**Target Audience:** High school student choosing engineering branch  
**Format:** Self-contained HTML files with embedded CSS/JS, speaker notes for AI video generation  
**Structure:** 20 slides per branch covering curriculum, careers, salaries, trends, AI impact, pros/cons

**Scope:** Originally 7 branches, expanded to cover all major engineering disciplines (22 total branches)

**Workflow:** See `generic_task.md` for step-by-step execution process

---

## Current Status Summary

**Completed:** 6 branches (EC, EE, CSE, ME, CE, Aerospace)  
**Remaining:** 16 branches across core, specialized, and emerging fields

---

## Completed Branches

### ✅ COMPLETED: EC (Electronics & Communication) Pilot

**Files:**
- `slides/EC.html` - 20/20 slides complete with 3 working images
- `slides/EC_Engineering_Career_Guide.mp4` - 38 MB video version
- `docs/EC.md` - Markdown version of all content
- `README.md` - Comprehensive documentation
- Design docs in `/docs/` folder (architecture, content outline, technical specs, implementation plan)

**Features Complete:**
- All 20 slides with comprehensive content
- Speaker notes (200-500+ words per slide)
- 3 Unsplash images with proper attribution
- Full navigation (keyboard, mouse, touch)
- Responsive design
- Accessibility (ARIA, WCAG AA)
- GitHub repository: https://github.com/tarakbluru/engineering-branch-slides (PUBLIC)
- GitHub Pages: https://tarakbluru.github.io/engineering-branch-slides/slides/EC.html

**Status:** Ready for user (daughter) review and feedback

### ✅ COMPLETED: EE (Electrical Engineering)

**Files:**
- `slides/EE.html` - 20/20 slides complete with 3 working images
- `docs/EE.md` - Markdown version of all content

**Features Complete:**
- All 20 slides with comprehensive EE content
- EE Gold branding (#FFB800, #FFCA33, #CC9400)
- Speaker notes (200-500+ words per slide)
- 3 Unsplash images with proper attribution
- Complete coverage: curriculum, careers, salaries, trends, AI impact, pros/cons
- Built from template.html following best practices

**Status:** Complete and deployed to GitHub Pages

### ✅ COMPLETED: CSE (Computer Science & Engineering)

**Files:**
- `slides/CSE.html` - 20/20 slides complete with 3 working images
- `slides/CSE__Complete_Guide.mp4` - 44 MB video version
- `docs/CSE.md` - Markdown version of all content

**Features Complete:**
- All 20 slides with comprehensive CSE content
- CSE Blue branding (#0066CC, #3399FF, #004C99)
- Speaker notes (200-500+ words per slide)
- 3 Unsplash images with proper attribution
- Complete coverage: curriculum, careers, salaries, trends, AI impact, pros/cons
- Built from template.html following best practices

**Status:** Complete and deployed to GitHub Pages

### ✅ COMPLETED: ME (Mechanical Engineering) - BONUS BRANCH

**Files:**
- `slides/ME.html` - 20/20 slides complete with 3 working images
- `slides/Mechanical_Engineering_Guide.mp4` - 43 MB video version
- `docs/ME.md` - Markdown version of all content

**Features Complete:**
- All 20 slides with comprehensive ME content
- ME branding with appropriate color scheme
- Speaker notes (200-500+ words per slide)
- 3 Unsplash images with proper attribution
- Complete coverage: curriculum, careers, salaries, trends, AI impact, pros/cons

**Status:** Complete and deployed to GitHub Pages

### ✅ COMPLETED: CE (Civil Engineering)

**Files:**
- `slides/CE.html` - 20/20 slides complete with 3 working images
- `docs/CE.md` - Comprehensive 25,000-word markdown guide

**Features Complete:**
- All 20 slides with comprehensive CE content
- Terra Cotta branding (#DC582A, #F08A65, #B24020)
- Speaker notes (200-500+ words per slide)
- Complete coverage: curriculum, careers (₹3-50+ LPA), salaries, trends, AI impact, pros/cons

**Status:** Complete and deployed to GitHub Pages

### ✅ COMPLETED: Aerospace Engineering

**Files:**
- `slides/Aerospace.html` - 20/20 slides complete with 3 working images
- `docs/Aerospace.md` - 160KB comprehensive guide (1,293 lines)
- `resources/aerospace_engineering_syllabus.md` - 17KB research compilation

**Features Complete:**
- All 20 slides with comprehensive Aerospace content
- Sky Blue branding (#0369A1, #0284C7, #075985)
- Speaker notes (200-500+ words per slide)
- Complete coverage: curriculum, careers (₹4.5-40+ LPA), ISRO/HAL/Boeing, AI impact, trends
- Research from IIT/NIT syllabi, industry data

**Status:** Complete and deployed to GitHub Pages

### ✅ COMPLETED: Templates for All Branches

**Template Files Created:**
- `docs/template.md` - Markdown template with placeholders and instructions for creating branch `.md` files
- `docs/template.html` - HTML template with placeholders and instructions for creating branch `.html` files

**Purpose:**
- **template.md** - Use for creating content in markdown format for notebook LLM video generation
- **template.html** - ⚠️ **ALWAYS use this as starting point for HTML files** (not existing branch files)

**Features:**
- Placeholder format: `[BRANCH_NAME]`, `[PRIMARY_COLOR]`, etc.
- Comprehensive instructions and comments
- All 20 slides structure pre-built
- Color scheme reference for all 7 branches
- Completion checklist included

---

## All Engineering Branches - Complete List

### **Category 1: Core Computer Science & IT (Original Priority)**

**Status: 3/7 Complete**

1. ✅ **CSE** - Computer Science & Engineering (COMPLETED)
2. ✅ **EC** - Electronics & Communication (COMPLETED)
3. ❌ **IS** - Information Science (TO DO)
4. ❌ **CSE-DS** - CSE (Data Science specialization) (TO DO)
5. ❌ **CSE-AIML** - CSE (AI & Machine Learning specialization) (TO DO)
6. ❌ **CSE-CS** - CSE (Cyber Security specialization) (TO DO)
7. ❌ **IT** - Information Technology (TO DO)

**Color Schemes:**
- IS: Teal (#00A896, #33BBAD, #008577)
- CSE-DS: Purple (#8B5CF6, #A78BFA, #7C3AED)
- CSE-AIML: Indigo (#4F46E5, #6366F1, #4338CA)
- CSE-CS: Navy (#1E3A8A, #3B82F6, #1E40AF)
- IT: Sky Blue (#0EA5E9, #38BDF8, #0284C7)

---

### **Category 2: Core Electrical & Electronics**

**Status: 2/3 Complete**

1. ✅ **EE** - Electrical Engineering (COMPLETED)
2. ✅ **EC** - Electronics & Communication (COMPLETED)
3. ❌ **Instrumentation** - Instrumentation & Control Engineering (TO DO)

**Color Schemes:**
- Instrumentation: Deep Purple (#6B21A8, #9333EA, #581C87)

---

### **Category 3: Core Mechanical & Manufacturing**

**Status: 1/4 Complete**

1. ✅ **ME** - Mechanical Engineering (COMPLETED)
2. ❌ **Automobile** - Automobile Engineering (TO DO)
3. ❌ **Aerospace** - Aerospace Engineering (TO DO)
4. ❌ **Production** - Production/Industrial Engineering (TO DO)

**Color Schemes:**
- Automobile: Racing Red (#DC2626, #EF4444, #B91C1C)
- Aerospace: Sky Blue (#0369A1, #0284C7, #075985)
- Production: Steel Gray (#475569, #64748B, #334155)

---

### **Category 4: Core Infrastructure & Construction**

**Status: 1/1 Complete**

1. ✅ **CE** - Civil Engineering (COMPLETED)

---

### **Category 5: Chemical & Process Engineering**

**Status: 0/2 Complete**

1. ❌ **Chemical** - Chemical Engineering (TO DO)
2. ❌ **Petroleum** - Petroleum Engineering (TO DO)

**Color Schemes:**
- Chemical: Forest Green (#16A34A, #22C55E, #15803D)
- Petroleum: Dark Blue (#1E40AF, #3B82F6, #1E3A8A)

---

### **Category 6: Emerging Technologies**

**Status: 0/5 Complete**

1. ❌ **Robotics** - Robotics & Automation Engineering (TO DO)
2. ❌ **Renewable** - Renewable Energy Engineering (TO DO)
3. ❌ **Biotech** - Biotechnology Engineering (TO DO)
4. ❌ **Environmental** - Environmental Engineering (TO DO)
5. ❌ **Mechatronics** - Mechatronics Engineering (TO DO)

**Color Schemes:**
- Robotics: Electric Blue (#2563EB, #3B82F6, #1D4ED8)
- Renewable: Lime Green (#65A30D, #84CC16, #4D7C0F)
- Biotech: Teal Blue (#0D9488, #14B8A6, #0F766E)
- Environmental: Nature Green (#059669, #10B981, #047857)
- Mechatronics: Orange (#EA580C, #F97316, #C2410C)

---

### **Category 7: Specialized Fields**

**Status: 0/3 Complete**

1. ❌ **Agricultural** - Agricultural Engineering (TO DO)
2. ❌ **Mining** - Mining Engineering (TO DO)
3. ❌ **Textile** - Textile Engineering (TO DO)

**Color Schemes:**
- Agricultural: Wheat Gold (#CA8A04, #EAB308, #A16207)
- Mining: Coal Black (#18181B, #27272A, #09090B)
- Textile: Magenta (#C026D3, #D946EF, #A21CAF)

---

## **Total Branches:**
- **Completed:** 5 (CSE, EC, EE, ME, CE)
- **Remaining:** 17
- **Grand Total:** 22 engineering branches

---

## Next Steps (Priority Order)

### **Phase 1: Complete Original 7 (Priority: HIGH)**
Finish the 4 remaining CSE/IT specializations from original plan:
1. IS - Information Science
2. CSE-DS - Data Science
3. CSE-AIML - AI & Machine Learning
4. CSE-CS - Cyber Security

### **Phase 2: Core Traditional Branches (Priority: MEDIUM)**
Popular traditional engineering branches:
1. Chemical Engineering
2. Aerospace Engineering
3. Automobile Engineering
4. Instrumentation Engineering

### **Phase 3: Emerging Fields (Priority: MEDIUM)**
Modern, high-growth branches:
1. Robotics & Automation
2. Renewable Energy
3. Biotechnology
4. Environmental Engineering

### **Phase 4: Specialized Fields (Priority: LOW)**
Niche but important branches:
1. Production/Industrial Engineering
2. Mechatronics
3. Agricultural Engineering
4. IT (Information Technology)
5. Petroleum Engineering
6. Mining Engineering
7. Textile Engineering

**Execution:** Follow the workflow in `generic_task.md` for creating each branch.

---

## Optional Enhancements (Future)

- Create index page linking all engineering branches
- Add comparison matrix across branches
- Add quiz/self-assessment tool
- Create videos for remaining branches
- Add more images throughout slides

---

## Repository Information

- **GitHub:** https://github.com/tarakbluru/engineering-branch-slides
- **GitHub Pages:** https://tarakbluru.github.io/engineering-branch-slides/
- **Visibility:** PUBLIC
- **Branch:** master

---

## Engineering Branch Color Schemes

**Core Computer Science & IT:**
- CSE: Primary #0066CC, Secondary #3399FF, Accent #004C99
- EC: Primary #FF6600, Secondary #FF8833, Accent #CC5200
- IS: Primary #00A896, Secondary #33BBAD, Accent #008577
- CSE-DS: Primary #8B5CF6, Secondary #A78BFA, Accent #7C3AED
- CSE-AIML: Primary #4F46E5, Secondary #6366F1, Accent #4338CA
- CSE-CS: Primary #1E3A8A, Secondary #3B82F6, Accent #1E40AF
- IT: Primary #0EA5E9, Secondary #38BDF8, Accent #0284C7

**Core Electrical & Electronics:**
- EE: Primary #FFB800, Secondary #FFCA33, Accent #CC9400
- Instrumentation: Primary #6B21A8, Secondary #9333EA, Accent #581C87

**Core Mechanical & Manufacturing:**
- ME: Primary #64748B, Secondary #94A3B8, Accent #475569
- Automobile: Primary #DC2626, Secondary #EF4444, Accent #B91C1C
- Aerospace: Primary #0369A1, Secondary #0284C7, Accent #075985
- Production: Primary #475569, Secondary #64748B, Accent #334155

**Core Infrastructure:**
- CE: Primary #DC582A, Secondary #F08A65, Accent #B24020

**Chemical & Process:**
- Chemical: Primary #16A34A, Secondary #22C55E, Accent #15803D
- Petroleum: Primary #1E40AF, Secondary #3B82F6, Accent #1E3A8A

**Emerging Technologies:**
- Robotics: Primary #2563EB, Secondary #3B82F6, Accent #1D4ED8
- Renewable: Primary #65A30D, Secondary #84CC16, Accent #4D7C0F
- Biotech: Primary #0D9488, Secondary #14B8A6, Accent #0F766E
- Environmental: Primary #059669, Secondary #10B981, Accent #047857
- Mechatronics: Primary #EA580C, Secondary #F97316, Accent #C2410C

**Specialized Fields:**
- Agricultural: Primary #CA8A04, Secondary #EAB308, Accent #A16207
- Mining: Primary #18181B, Secondary #27272A, Accent #09090B
- Textile: Primary #C026D3, Secondary #D946EF, Accent #A21CAF

---

**Last Updated:** June 13, 2026  
**Status:** 6 branches complete (EC, EE, CSE, ME, CE, Aerospace) - 16 remaining

**For execution workflow, see:** `generic_task.md`

**Templates Available:**
- ✅ `docs/template.md` - Markdown template with full instructions
- ✅ `docs/template.html` - HTML template with full instructions ⚠️ **ALWAYS use this as starting point**
- Both templates include all 20 slides structure with placeholder guidance
