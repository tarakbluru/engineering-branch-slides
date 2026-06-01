# HTML Slide Deck - Technical Specification

## Document Purpose
This document defines the technical implementation details for the HTML slide deck, including structure, styling, navigation, and AI-readability features.

## HTML Document Structure

### Overall File Architecture

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="[Branch Name] Engineering - Complete Guide">
    <title>[Branch Name] Engineering | Career & Curriculum Guide</title>
    
    <!-- Embedded CSS -->
    <style>
        /* Global Styles */
        /* Layout Styles */
        /* Slide Styles */
        /* Navigation Styles */
        /* Responsive Styles */
    </style>
</head>
<body>
    <!-- Navigation Controls -->
    <nav class="slide-nav">
        <!-- Progress bar, slide counter, next/prev buttons -->
    </nav>
    
    <!-- Slide Container -->
    <main class="slides-container">
        <!-- Slide 1 -->
        <section class="slide active" id="slide-1" data-slide-number="1">
            <!-- Slide content -->
            <aside class="speaker-notes">
                <!-- Speaker notes for AI narration -->
            </aside>
        </section>
        
        <!-- Slide 2 -->
        <section class="slide" id="slide-2" data-slide-number="2">
            <!-- Slide content -->
            <aside class="speaker-notes">
                <!-- Speaker notes -->
            </aside>
        </section>
        
        <!-- ... Additional slides ... -->
    </main>
    
    <!-- Embedded JavaScript -->
    <script>
        /* Navigation logic */
        /* Keyboard controls */
        /* Progress tracking */
    </script>
</body>
</html>
```

---

## CSS Styling Specifications

### 1. Global Styles

```css
/* Reset and Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    /* Branch-specific color variables */
    --primary-color: #[BRANCH_COLOR];
    --secondary-color: #[COMPLEMENTARY_COLOR];
    --text-dark: #222222;
    --text-light: #666666;
    --background: #FFFFFF;
    --accent: #[ACCENT_COLOR];
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 18px;
    line-height: 1.6;
    color: var(--text-dark);
    background: var(--background);
    overflow: hidden; /* Prevent scrolling during presentation */
}

/* Typography */
h1 {
    font-size: 3rem;
    font-weight: 700;
    color: var(--primary-color);
    margin-bottom: 1rem;
}

h2 {
    font-size: 2.5rem;
    font-weight: 600;
    color: var(--primary-color);
    margin-bottom: 0.8rem;
}

h3 {
    font-size: 1.8rem;
    font-weight: 600;
    margin-bottom: 0.6rem;
}

p {
    font-size: 1.1rem;
    margin-bottom: 1rem;
}

ul, ol {
    margin-left: 2rem;
    margin-bottom: 1rem;
}

li {
    margin-bottom: 0.5rem;
    font-size: 1.1rem;
}
```

### 2. Slide Container Styles

```css
.slides-container {
    width: 100vw;
    height: 100vh;
    position: relative;
    overflow: hidden;
}

.slide {
    position: absolute;
    width: 100%;
    height: 100%;
    padding: 4rem 6rem;
    display: none; /* Hidden by default */
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    background: var(--background);
}

.slide.active {
    display: flex; /* Show active slide */
}

/* Slide Layout Variants */

/* Title Slide Layout */
.slide.title-slide {
    justify-content: center;
    align-items: center;
    text-align: center;
    background-size: cover;
    background-position: center;
    position: relative;
}

.slide.title-slide::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.5); /* Dark overlay for text readability */
}

.slide.title-slide .content {
    position: relative;
    z-index: 1;
    color: white;
}

/* Two-Column Layout */
.slide.two-column {
    flex-direction: row;
    gap: 3rem;
}

.slide.two-column .column {
    flex: 1;
}

.slide.two-column .column-left {
    flex: 0.6;
}

.slide.two-column .column-right {
    flex: 0.4;
}

/* Grid Layout for Skills/Cards */
.slide .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
    width: 100%;
}

.card {
    background: #f5f5f5;
    border-left: 4px solid var(--primary-color);
    padding: 1.5rem;
    border-radius: 8px;
}
```

### 3. Navigation Styles

```css
.slide-nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    background: rgba(255, 255, 255, 0.95);
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    padding: 0.5rem 2rem;
}

.progress-bar {
    position: absolute;
    top: 0;
    left: 0;
    height: 4px;
    background: var(--primary-color);
    transition: width 0.3s ease;
}

.slide-counter {
    position: absolute;
    top: 1rem;
    right: 2rem;
    font-size: 0.9rem;
    color: var(--text-light);
}

.nav-buttons {
    position: fixed;
    bottom: 2rem;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    padding: 0 2rem;
    z-index: 1000;
}

button.nav-btn {
    background: var(--primary-color);
    color: white;
    border: none;
    padding: 0.8rem 1.5rem;
    font-size: 1rem;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s ease;
}

button.nav-btn:hover {
    background: var(--secondary-color);
}

button.nav-btn:disabled {
    background: #cccccc;
    cursor: not-allowed;
}
```

### 4. Speaker Notes Styles

```css
.speaker-notes {
    display: none; /* Hidden in presentation view */
    background: #f9f9f9;
    border-left: 4px solid var(--accent);
    padding: 1rem;
    margin-top: 2rem;
    font-size: 0.95rem;
    color: var(--text-light);
}

/* For AI parsing and print view */
@media print {
    .speaker-notes {
        display: block;
        page-break-before: avoid;
    }
    
    .slide {
        page-break-after: always;
    }
}

/* Speaker notes can be toggled visible with a class */
body.show-notes .speaker-notes {
    display: block;
}
```

### 5. Image & Media Styles

```css
.slide img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.image-caption {
    font-size: 0.85rem;
    color: var(--text-light);
    font-style: italic;
    margin-top: 0.5rem;
    text-align: center;
}

.video-link {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--primary-color);
    text-decoration: none;
    padding: 0.5rem 1rem;
    border: 2px solid var(--primary-color);
    border-radius: 5px;
    transition: all 0.3s ease;
}

.video-link:hover {
    background: var(--primary-color);
    color: white;
}
```

### 6. Responsive Styles

```css
@media screen and (max-width: 1024px) {
    .slide {
        padding: 3rem 4rem;
    }
    
    h1 { font-size: 2.5rem; }
    h2 { font-size: 2rem; }
    h3 { font-size: 1.5rem; }
    
    .slide.two-column {
        flex-direction: column;
    }
}

@media screen and (max-width: 768px) {
    .slide {
        padding: 2rem;
    }
    
    h1 { font-size: 2rem; }
    h2 { font-size: 1.6rem; }
    
    .card-grid {
        grid-template-columns: 1fr;
    }
}
```

---

## JavaScript Functionality Specifications

### 1. Core Navigation Functions

```javascript
// Global state
let currentSlide = 1;
const totalSlides = document.querySelectorAll('.slide').length;

// Initialize on page load
function init() {
    updateProgressBar();
    updateSlideCounter();
    updateNavigationButtons();
    setupKeyboardControls();
    showSlide(1);
}

// Navigate to specific slide
function showSlide(slideNumber) {
    // Hide all slides
    document.querySelectorAll('.slide').forEach(slide => {
        slide.classList.remove('active');
    });
    
    // Show target slide
    const targetSlide = document.querySelector(`[data-slide-number="${slideNumber}"]`);
    if (targetSlide) {
        targetSlide.classList.add('active');
        currentSlide = slideNumber;
        updateProgressBar();
        updateSlideCounter();
        updateNavigationButtons();
    }
}

// Navigation controls
function nextSlide() {
    if (currentSlide < totalSlides) {
        showSlide(currentSlide + 1);
    }
}

function prevSlide() {
    if (currentSlide > 1) {
        showSlide(currentSlide - 1);
    }
}

// Update progress bar
function updateProgressBar() {
    const progress = (currentSlide / totalSlides) * 100;
    document.querySelector('.progress-bar').style.width = progress + '%';
}

// Update slide counter
function updateSlideCounter() {
    document.querySelector('.slide-counter').textContent = 
        `Slide ${currentSlide} of ${totalSlides}`;
}

// Enable/disable navigation buttons
function updateNavigationButtons() {
    const prevBtn = document.querySelector('#prev-btn');
    const nextBtn = document.querySelector('#next-btn');
    
    prevBtn.disabled = (currentSlide === 1);
    nextBtn.disabled = (currentSlide === totalSlides);
}

// Keyboard controls
function setupKeyboardControls() {
    document.addEventListener('keydown', (e) => {
        switch(e.key) {
            case 'ArrowRight':
            case 'ArrowDown':
            case ' ': // Spacebar
                e.preventDefault();
                nextSlide();
                break;
            case 'ArrowLeft':
            case 'ArrowUp':
                e.preventDefault();
                prevSlide();
                break;
            case 'Home':
                e.preventDefault();
                showSlide(1);
                break;
            case 'End':
                e.preventDefault();
                showSlide(totalSlides);
                break;
            case 'n': // Toggle notes (for presenter mode)
                document.body.classList.toggle('show-notes');
                break;
        }
    });
}

// Initialize when DOM is ready
document.addEventListener('DOMContentLoaded', init);
```

### 2. Touch/Swipe Support (for tablets)

```javascript
let touchStartX = 0;
let touchEndX = 0;

function handleSwipe() {
    const swipeThreshold = 50; // minimum distance for swipe
    const diff = touchEndX - touchStartX;
    
    if (Math.abs(diff) > swipeThreshold) {
        if (diff > 0) {
            prevSlide(); // Swipe right
        } else {
            nextSlide(); // Swipe left
        }
    }
}

document.addEventListener('touchstart', (e) => {
    touchStartX = e.changedTouches[0].screenX;
});

document.addEventListener('touchend', (e) => {
    touchEndX = e.changedTouches[0].screenX;
    handleSwipe();
});
```

---

## AI-Readability Features

### 1. Structured Data for AI Parsing

Each slide will include metadata attributes:

```html
<section class="slide" 
         id="slide-1" 
         data-slide-number="1"
         data-slide-type="title"
         data-slide-title="[Slide Title]">
    
    <!-- Visible content -->
    <div class="content">
        <!-- Slide content here -->
    </div>
    
    <!-- Speaker notes for AI narration -->
    <aside class="speaker-notes" 
           data-duration="45"
           data-tone="engaging">
        <h4>Narration Script:</h4>
        <p>[Detailed narration text...]</p>
        
        <h4>Key Points:</h4>
        <ul>
            <li>[Point 1]</li>
            <li>[Point 2]</li>
        </ul>
        
        <h4>Context:</h4>
        <p>[Why this slide matters...]</p>
    </aside>
</section>
```

### 2. Semantic HTML for AI Understanding

Use proper semantic elements:

```html
<article class="topic">
    <header>
        <h2>[Topic Title]</h2>
    </header>
    
    <section class="description">
        <p>[Content]</p>
    </section>
    
    <footer class="source">
        <cite>Source: [Citation]</cite>
    </footer>
</article>
```

### 3. Image Descriptions for AI

```html
<figure>
    <img src="[URL]" 
         alt="[Detailed description for AI and accessibility]"
         data-ai-description="[Extended description for AI narration]">
    <figcaption class="image-caption">
        [Caption text]
        <span class="attribution">Image: [Source]</span>
    </figcaption>
</figure>
```

---

## Accessibility Features

### 1. ARIA Labels

```html
<nav class="slide-nav" role="navigation" aria-label="Slide navigation">
    <button id="prev-btn" 
            aria-label="Previous slide" 
            class="nav-btn">
        ← Previous
    </button>
    
    <button id="next-btn" 
            aria-label="Next slide" 
            class="nav-btn">
        Next →
    </button>
</nav>

<div class="slide-counter" 
     role="status" 
     aria-live="polite" 
     aria-atomic="true">
    Slide 1 of 20
</div>
```

### 2. Keyboard Navigation

- **Arrow keys**: Next/Previous slide
- **Spacebar**: Next slide
- **Home**: First slide
- **End**: Last slide
- **N key**: Toggle speaker notes visibility

### 3. Screen Reader Support

```html
<!-- Skip to content link -->
<a href="#main-content" class="skip-link">Skip to main content</a>

<!-- Slide announcements -->
<div class="sr-only" aria-live="assertive">
    Now showing: [Slide Title]
</div>
```

---

## Color Schemes by Branch

### CSE (Computer Science & Engineering)
```css
:root {
    --primary-color: #0066CC;     /* Blue */
    --secondary-color: #0099FF;   /* Light Blue */
    --accent: #00CCFF;            /* Cyan */
}
```

### EC (Electronics & Communication)
```css
:root {
    --primary-color: #FF6600;     /* Orange */
    --secondary-color: #FF8833;   /* Light Orange */
    --accent: #CC5200;            /* Dark Orange */
}
```

### EE (Electrical Engineering)
```css
:root {
    --primary-color: #FFB800;     /* Gold */
    --secondary-color: #FFCC33;   /* Light Gold */
    --accent: #FF9900;            /* Amber */
}
```

### Information Science
```css
:root {
    --primary-color: #00AA66;     /* Green */
    --secondary-color: #00CC7A;   /* Light Green */
    --accent: #008855;            /* Teal */
}
```

### CSE - Data Science
```css
:root {
    --primary-color: #9933CC;     /* Purple */
    --secondary-color: #AA55DD;   /* Light Purple */
    --accent: #7722AA;            /* Dark Purple */
}
```

### CSE - AI & ML
```css
:root {
    --primary-color: #4466FF;     /* Blue-Purple */
    --secondary-color: #6688FF;   /* Light Blue-Purple */
    --accent: #2244CC;            /* Dark Blue-Purple */
}
```

### CSE - Cyber Security
```css
:root {
    --primary-color: #CC0000;     /* Red */
    --secondary-color: #001F3F;   /* Navy Blue */
    --accent: #FF3333;            /* Bright Red */
}
```

---

## File Size & Performance Considerations

### Optimization Strategies

1. **Images**:
   - Use web URLs (no embedded images)
   - Lazy loading for off-screen images
   - Specify image dimensions to prevent layout shift

2. **CSS**:
   - Minification (optional, but keeps file readable for now)
   - No unused styles
   - Critical CSS inline

3. **JavaScript**:
   - Vanilla JS (no libraries)
   - Minimal DOM manipulation
   - Event delegation where possible

4. **Target File Size**:
   - Each HTML file: < 200 KB (including embedded CSS/JS)
   - Fast loading on slow connections
   - Works offline (except external images)

---

## Browser Compatibility

### Target Browsers
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

### Fallbacks
- CSS Grid with flexbox fallback
- Modern JavaScript with no transpilation required (ES6+)
- Progressive enhancement approach

---

## Export & Sharing Options

### Built-in Features

1. **Print to PDF**:
   - Browser's print function creates a PDF
   - Speaker notes included in print version
   - Each slide on separate page

2. **Speaker Notes Toggle**:
   - Press 'N' to show/hide notes during presentation
   - Useful for presenter mode or AI parsing

3. **Direct Sharing**:
   - Single HTML file can be emailed or uploaded
   - No dependencies (works as standalone file)
   - Can be hosted on any web server

---

## Quality Checklist for Implementation

Before marking a slide deck complete, verify:

**Technical**:
- [ ] All slides navigate correctly
- [ ] Progress bar updates accurately
- [ ] Keyboard controls work
- [ ] Touch/swipe works on mobile
- [ ] No console errors
- [ ] Links open in new tabs
- [ ] Images load properly

**Content**:
- [ ] All speaker notes are 150-300 words
- [ ] Each slide has proper semantic HTML
- [ ] Images have alt text and attributions
- [ ] Sources are cited
- [ ] Video links are functional

**Accessibility**:
- [ ] ARIA labels present
- [ ] Color contrast meets WCAG AA
- [ ] Keyboard navigation complete
- [ ] Screen reader tested

**AI-Readability**:
- [ ] Speaker notes are comprehensive
- [ ] Slide metadata attributes present
- [ ] Semantic HTML structure
- [ ] Image descriptions detailed

---

## Sample HTML Template Structure (Pseudocode)

This is the conceptual structure (actual implementation in Phase 4):

```
HTML File: EC.html
├── <head>
│   ├── Meta tags
│   ├── Title
│   └── <style> [Embedded CSS - all styling]
│
├── <body>
│   ├── <nav> Navigation controls
│   │   ├── Progress bar
│   │   ├── Slide counter
│   │   └── Next/Prev buttons
│   │
│   ├── <main> Slides container
│   │   ├── <section class="slide"> Slide 1 - Title
│   │   │   ├── Content
│   │   │   └── <aside> Speaker notes
│   │   │
│   │   ├── <section class="slide"> Slide 2 - Overview
│   │   │   ├── Content
│   │   │   └── <aside> Speaker notes
│   │   │
│   │   ├── ... [Slides 3-18]
│   │   │
│   │   └── <section class="slide"> Slide 20 - Checklist
│   │       ├── Content
│   │       └── <aside> Speaker notes
│   │
│   └── <script> [Embedded JavaScript - all functionality]
```

---

## Next Phase: Implementation

Once this design is approved, Phase 3 will create an implementation plan, and Phase 4 will generate:

1. **Template HTML file** (generic structure)
2. **EC.html** (Electronics & Communication pilot)

Both will follow these specifications exactly.
