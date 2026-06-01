# Project Tasks - Engineering Branch Slide Decks

## Project Overview
Create interactive HTML slide decks for 7 engineering branches to help a high school student (daughter) evaluate career options.

**Target Audience:** High school student choosing engineering branch  
**Format:** Self-contained HTML files with embedded CSS/JS, speaker notes for AI video generation  
**Structure:** 20 slides per branch covering curriculum, careers, salaries, trends, AI impact, pros/cons

---

## Current Status

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

---

## Next Steps (Priority Order)

### 1. GET USER FEEDBACK on EC Pilot
- Share EC.html with daughter
- Gather feedback on content, presentation, clarity
- Note what works well and what needs improvement
- Adjust template based on feedback before replicating

### 2. CREATE REMAINING 6 BRANCHES (After EC Approval)

Each branch follows the same 20-slide structure as EC:

**Branches to Create:**
1. **CSE** - Computer Science & Engineering
2. **EE** - Electrical Engineering
3. **IS** - Information Science
4. **CSE-DS** - CSE (Data Science)
5. **CSE-AIML** - CSE (AI & Machine Learning)
6. **CSE-CS** - CSE (Cyber Security)

**Process per Branch:**
1. Research content (curriculum, careers, salaries, trends)
2. Adapt template with branch-specific content
3. Find 3 relevant images (Unsplash with attribution)
4. Write comprehensive speaker notes (200-500 words/slide)
5. Test navigation and responsiveness
6. Commit and push to GitHub
7. Verify on GitHub Pages

### 3. OPTIONAL ENHANCEMENTS (After All 7 Complete)

- Create index page linking all 7 branches
- Add comparison matrix across branches
- Add quiz/self-assessment tool
- Create videos for remaining branches
- Add more images throughout slides

---

## Key Information

### Repository
- **GitHub:** https://github.com/tarakbluru/engineering-branch-slides
- **GitHub Pages:** https://tarakbluru.github.io/engineering-branch-slides/
- **Visibility:** PUBLIC
- **Branch:** master

### File Structure
```
engineering-branch-slides/
├── README.md                   # Comprehensive documentation
├── TASK.md                     # This file
├── .claude/CLAUDE.md           # Project configuration
├── docs/
│   ├── 01_template_architecture.md
│   ├── 02_content_outline.md
│   ├── 03_html_technical_spec.md
│   ├── 04_ec_pilot_implementation_plan.md
│   └── EC.md                   # EC content in markdown
└── slides/
    ├── EC.html                 # ✅ Complete
    └── EC_Engineering_Career_Guide.mp4
```

### Template Structure (20 Slides)
1. Title - Branch branding
2. Overview - What is this branch
3-5. Curriculum - Years 1-4, courses, labs
6. Skills - Technical, tools, professional
7-8. Careers - Entry to senior roles, salaries
9. Industry Sectors - Where graduates work
10. Higher Education - MS/PhD options
11. Day-to-Day Work - Realistic scenario
12. Compensation - India + international salaries
13. Current Trends - What's hot in the field
14-15. AI Impact - How AI transforms field, future strategy
16. Educational Resources - Videos, courses, books
17. Real-World Projects - Student and industry examples
18. Pros & Cons - Honest assessment
19. Decision Checklist - Self-assessment
20. Closing - Summary and key takeaways

### Content Sources
- **Academic:** MIT OCW, IIT curricula, IEEE, ACM
- **Industry:** LinkedIn, Glassdoor, company career pages
- **Educational:** YouTube channels, Coursera, edX, NPTEL
- **Images:** Unsplash.com (free with attribution)

### Technical Details
- Self-contained HTML (no external dependencies)
- Embedded CSS and JavaScript
- Branch-specific color schemes (EC = Orange #FF6600)
- Navigation: Arrow keys, spacebar, mouse, touch/swipe
- Press 'N' to toggle speaker notes
- Works offline except images
- Optimized for web (146 KB file size)

---

## Important Notes

### When Creating New Branches:
1. Copy EC.html as template
2. Update color scheme (see `03_html_technical_spec.md` for branch colors)
3. Replace ALL EC-specific content with new branch content
4. Find 3 relevant images from Unsplash (verify URLs work!)
5. Update speaker notes to match new content
6. Test locally before committing
7. Commit with descriptive message
8. Push to GitHub
9. Verify on GitHub Pages

### Image Guidelines:
- Use Unsplash URLs: `https://images.unsplash.com/photo-[ID]?w=800&q=80`
- Test URL works: `curl -I "URL"` should return HTTP 200
- Add proper alt text for accessibility
- Include attribution in caption: "Photo by [Name] on Unsplash"
- 3 images per branch (slides 2, 3, 4 typically)

### Git Workflow:
```bash
git add [files]
git commit -m "Descriptive message"
git push origin master
# GitHub Pages auto-rebuilds (wait 1-2 minutes)
```

### Testing Checklist per Branch:
- [ ] All 20 slides present
- [ ] Navigation works (next/prev buttons, keyboard)
- [ ] Progress bar updates correctly
- [ ] Images load properly
- [ ] Speaker notes toggle with 'N' key
- [ ] Responsive on mobile (test in browser dev tools)
- [ ] Works on GitHub Pages URL

---

## Current Blockers

**NONE** - EC pilot complete, awaiting user feedback.

---

## Questions for User (If Any)

1. Has daughter reviewed EC.html? Any feedback?
2. Any specific content preferences for remaining branches?
3. Any branches to prioritize over others?
4. Should we add video versions for all branches?

---

**Last Updated:** June 1, 2026  
**Status:** EC Complete - Ready for Feedback and Next Branch
