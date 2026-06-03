# EE.html Rebuild Plan

## Status: Ready to Start Fresh

**Previous Attempt:** EE.html was created by modifying CSE.html, but verification found issues:
- HTML comments still referenced CSE
- Some embedded CSE speaker notes remained  
- Slide count mismatch (19 instead of 20)
- Non-EE relevant images

**Decision:** Start fresh from template.html for clean, complete implementation

---

## Objective

Create complete `slides/EE.html` with all 20 slides containing accurate Electrical Engineering content.

---

## Source Files

1. **Template:** `docs/template.html` - Clean HTML template with [PLACEHOLDERS]
2. **Content Source:** `docs/EE.md` - Complete EE content for all 20 slides
3. **Reference:** `slides/CSE.html` - Working example of completed slides

---

## EE Branding

**Colors (from template.html reference):**
- Primary: `#FFB800` (Gold)
- Secondary: `#FFCA33` (Light Gold)
- Accent: `#CC9400` (Dark Gold)

**Branding:**
- Branch Name: "Electrical Engineering"
- Abbreviation: "EE"
- Tagline: "Powering the World - From Generation to Smart Grids"

---

## Implementation Steps

### Step 1: Copy Template
```bash
cp docs/template.html slides/EE.html
```

### Step 2: Replace Header Placeholders
In `<head>` section and top of `<style>`:
- `[BRANCH_NAME]` → "Electrical Engineering"
- `[PRIMARY_COLOR]` → `#FFB800`
- `[SECONDARY_COLOR]` → `#FFCA33`
- `[ACCENT]` → `#CC9400`

### Step 3: Fill All 20 Slides Systematically

**Content location:** All slide content is in `docs/EE.md`

**All 20 Slides:**
1. Title & Overview - EE introduction
2. What is EE? - Definition, fundamental areas (Power Systems, Electronics, Machines, Renewable)
3. Years 1-2 Curriculum - Foundation courses
4. Year 3 Curriculum - Power Systems, Machines, Power Electronics, Control
5. Year 4 Curriculum - Advanced (HVDC, Renewable, Drives), electives
6. Skills - Power analysis, machines, electronics, tools (MATLAB, ETAP, PLCs)
7. Entry-Level Careers - Salaries ₹4-16 LPA (Power Plant, T&D, Automation, Renewable, Power Electronics)
8. Career Growth - Mid/senior ₹12-50 LPA, alternative paths
9. Industries - NTPC, PGCIL, Siemens, ABB, Adani Green, Tata Power
10. Higher Education - M.Tech specializations (Power Systems, Power Electronics, HV, Control)
11. Day in Life - Power Plant Engineer scenario
12. Compensation - Detailed salary breakdown, market outlook
13. Current Trends - 500 GW renewable target, EVs, battery storage, power electronics
14. AI Transformation - Digitalization, IoT in power systems, predictive maintenance
15. Future Skills - Power fundamentals, renewable energy, automation, software
16. Educational Resources - YouTube (The Electrical Guy, GreatScott!), courses (NPTEL), books, software
17. Real Projects - Student projects (microgrid, motor drive) + Industry (Bhadla Solar, Delhi Metro)
18. Pros & Cons - Honest assessment, who thrives/struggles
19. Decision Framework - Self-assessment questions, next steps
20. Closing - Key takeaways, resources, stay curious/safe

### Step 4: Systematic Content Replacement

For each slide:
1. Read corresponding slide content from `docs/EE.md`
2. Replace [CONTENT] placeholder with slide body content
3. Replace [SPEAKER_NOTES] placeholder with speaker notes from EE.md
4. Update HTML comments (e.g., `<!-- Slide 2: What is EE? -->`)
5. Ensure proper HTML structure maintained

### Step 5: Image Selection

Find 3 appropriate Unsplash images for EE:
- Slide 2: Power plant/electrical systems
- Slide 3: Engineering students/lab work
- Slide 4: Solar panels/renewable energy or power lines

Test image URLs before adding:
```bash
curl -I "https://images.unsplash.com/photo-XXXXX?w=800&q=80"
```

### Step 6: Verification Checklist

Before committing, verify:
- [ ] All 20 slides present (count: `grep -c 'class="slide"' slides/EE.html` should return 20)
- [ ] No CSE references remain (check: `grep -i "computer science\|CSE\|software developer\|programming" slides/EE.html`)
- [ ] All HTML comments updated to EE (check comments manually)
- [ ] Color scheme correct (all #FFB800, #FFCA33, #CC9400)
- [ ] Title is "Electrical Engineering | Career Guide"
- [ ] All speaker notes are EE-specific
- [ ] Images are EE-relevant
- [ ] Navigation works (test in browser)
- [ ] Speaker notes toggle works (press 'N' key)

### Step 7: Testing

```bash
# Open in browser to test
firefox slides/EE.html  # or appropriate browser

# Test:
# - Arrow key navigation
# - Click navigation buttons
# - Press 'N' to toggle speaker notes
# - Check all 20 slides display correctly
# - Verify progress bar updates
```

### Step 8: Commit

```bash
git add slides/EE.html
git commit -m "Create EE.html from template.html - all 20 slides complete

Built properly from template.html with:
- All EE branding and colors (#FFB800 Gold)
- Complete content from EE.md for all 20 slides
- EE-specific images
- Verified: no CSE references, all comments updated, 20 slides confirmed

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"
git push origin master
```

---

## Key Content Points (from EE.md)

**Salaries:**
- Fresh: ₹3.5-6 LPA (Tier 2), ₹8-12 LPA (PSUs), ₹10-16 LPA (EV companies)
- Mid-level: ₹12-20 LPA, specialized ₹20-30 LPA
- Senior: ₹22-35 LPA, leadership ₹40 LPA - ₹1.5 Cr

**Major Companies:**
- PSUs: NTPC, PGCIL, NHPC, BHEL
- Private: Siemens, ABB, Schneider Electric, L&T
- Renewable: Adani Green, ReNew Power, Tata Power Solar
- EV: Tata Motors, Ather Energy, Ola Electric

**Key Trends:**
- India's 500 GW renewable energy target by 2030
- EV adoption and charging infrastructure
- Grid modernization and smart grids
- Battery storage systems
- Power electronics revolution (SiC, GaN)

**Educational Resources:**
- YouTube: The Electrical Guy, GreatScott!, ElectroBOOM, Andreas Spiess
- Courses: NPTEL (IIT Madras Solar Energy), Coursera Power Systems, MIT Renewable Energy
- Books: Hadi Saadat, P.S. Bimbhra, Ned Mohan
- Software: MATLAB/Simulink, ETAP, PowerWorld, AutoCAD Electrical, PLC programming

---

## Lessons Learned from Previous Attempt

**DON'T:**
- ❌ Start from CSE.html and replace content piece by piece
- ❌ Leave HTML comments unchanged
- ❌ Assume all content was replaced without verification
- ❌ Skip verification before declaring complete

**DO:**
- ✅ Start fresh from template.html
- ✅ Replace ALL placeholders systematically
- ✅ Update ALL HTML comments to match content
- ✅ Verify slide count (should be exactly 20)
- ✅ Search for any remaining CSE references before committing
- ✅ Test in browser before pushing

---

## Success Criteria

EE.html is complete when:
1. All 20 slides present with EE content
2. Zero CSE references (verified via grep)
3. All HTML comments reference EE (not CSE)
4. Colors are EE Gold theme throughout
5. Images are EE-relevant
6. Navigation and speaker notes work in browser
7. Content matches EE.md accurately
8. Passes verification checklist above

---

## Estimated Time

- Template setup: 5 minutes
- Content filling (20 slides): 60-90 minutes
- Image selection: 10 minutes
- Verification: 10 minutes
- Testing: 5 minutes

**Total: ~90-120 minutes for complete, verified EE.html**

---

## Next Session Instructions

When you read this file:
1. Execute the implementation steps above systematically
2. Use template.html as starting point (NOT CSE.html)
3. Reference EE.md for all content
4. Run verification checks before declaring complete
5. Test in browser to ensure functionality

Good luck! 🚀⚡
