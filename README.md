# CXO Resume Brand Guidelines & CSS Framework

## Design Philosophy
The CXO Resume brand embodies sophisticated editorial design inspired by The New Yorker and Financial Times, creating a premium experience appropriate for C-suite executives.

## Core CSS Variables

```css
:root {
  --bg: #fff1e5;          /* Financial Times pink background */
  --ink: #000;            /* Pure black for text */
  --muted: #666;          /* Gray for secondary text */
  --rule: #000;           /* Black for borders/rules */
  --soft: #ddd;           /* Light gray for subtle borders */
  --button-bg: #000;      /* Black button background */
  --button-color: #fff;   /* White button text */
  --button-hover-bg: #333; /* Dark gray on hover */
}
```

## Typography System

### Font Stack
```css
/* Primary fonts - always import these */
@import url('https://fonts.googleapis.com/css2?family=Aboreto:wght@400&family=Crimson+Text:ital,wght@0,400;0,600;1,400&family=IBM+Plex+Sans:wght@300;400;500&display=swap');
```

### Font Hierarchy

**1. Brand Title (THE CXO RESUME)**
```css
.magazine-title {
  font-family: 'Aboreto', serif;
  font-size: 56px;
  font-weight: 400;
  letter-spacing: 10px;
  color: var(--ink);
  margin: 0 0 6px 0;
  text-transform: uppercase;
}
@media (max-width: 600px){
  .magazine-title{ font-size:44px; letter-spacing:8px; }
}
```

**2. Navigation/Meta Info**
```css
.issue-info{
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:11px; 
  color:var(--muted);
  letter-spacing:1px; 
  text-transform:uppercase;
}
```

**3. Section Labels**
```css
.section-title{
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:11px; 
  color:#666;
  letter-spacing:2px; 
  text-transform:uppercase; 
  margin-bottom:20px; 
  font-weight:500;
}
```

**4. Article Titles**
```css
.article-title{
  font-size:36px; 
  font-weight:400; 
  line-height:1.1; 
  color:#000; 
  margin:0 0 20px 0;
}
```

**5. Article Subtitles**
```css
.article-subtitle{
  font-size:20px; 
  font-style:italic; 
  color:#555; 
  margin:0 0 30px 0; 
  font-weight:400;
}
```

**6. Body Text**
```css
.article-content{ 
  font-size:18px; 
  line-height:1.7; 
  color:#2c2c2c; 
  text-align:justify; 
  hyphens:auto; 
}
.article-content p{ margin:0 0 20px 0; }
```

**7. Subheadings**
```css
.subheading{ 
  font-size:22px; 
  font-weight:600; 
  color:#000; 
  margin:40px 0 20px 0; 
  line-height:1.3; 
}
```

## Layout Structure

### Base Body Layout
```css
body {
  font-family: 'Crimson Text', serif;
  font-size: 16px;
  line-height: 1.6;
  color: #2c2c2c;
  background-color: var(--bg);
  margin: 0;
  padding: 40px 20px;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}
```

### Masthead Pattern
```css
.masthead {
  text-align: center;
  border-bottom: 3px solid var(--rule);
  padding: 0 0 20px 0;
  margin: 0 0 40px 0;
}
```

### Article Header Pattern
```css
.article-header{ margin:60px 0 40px 0; }
```

## Interactive Elements

### Primary CTA Box Pattern
```css
.case-box{
  border:1px solid #dadada;   /* Light gray border - NEVER black */
  padding:28px;
  margin:30px 0;
  text-align:center;
  background:transparent;
}
.case-title{
  font-family:'Aboreto',serif; 
  font-size:24px; 
  font-weight:400; 
  color:#000; 
  margin:0 0 14px 0; 
  letter-spacing:2px; 
  text-transform:uppercase;
}
.case-lead{
  font-family:'Crimson Text',serif; 
  font-size:16px; 
  color:#555; 
  margin:0 0 22px 0; 
  line-height:1.5;
}
.case-button{
  background-color:#000; 
  color:#fff; 
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:14px; 
  font-weight:500;
  text-transform:uppercase; 
  letter-spacing:2px; 
  padding:15px 40px; 
  border:none; 
  cursor:pointer; 
  display:inline-block;
  transition: background-color .25s;
}
.case-button:hover{ background-color:#333; }
```

### Secondary CTA Box Pattern
```css
.cta-box{
  background-color:var(--bg);
  border:1px solid #ddd; 
  margin:40px 0; 
  padding:30px; 
  text-align:center;
}
.cta-title{
  font-family:'Aboreto',serif; 
  font-size:24px; 
  font-weight:400; 
  color:#000; 
  margin:0 0 15px 0; 
  letter-spacing:2px; 
  text-transform:uppercase;
}
.cta-description{
  font-family:'Crimson Text',serif; 
  font-size:16px; 
  color:#555; 
  margin:0 0 25px 0; 
  line-height:1.5;
}
.cta-button{
  background-color:#000; 
  color:#fff; 
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:14px; 
  font-weight:500;
  text-transform:uppercase; 
  letter-spacing:2px; 
  padding:15px 40px; 
  border:none; 
  cursor:pointer; 
  text-decoration:none; 
  display:inline-block; 
  margin-bottom:20px;
  transition: background-color .25s;
}
.cta-button:hover{ background-color:#333; }
.cta-legal{ 
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:12px; 
  color:#777; 
  line-height:1.4; 
  margin:0; 
}
.cta-legal a{ color:#000; text-decoration:underline; }
```

### Navigation Links
```css
.meta-link{ 
  position:relative; 
  text-decoration:none; 
  color:#444; 
  padding-bottom:2px; 
}
.meta-link::after{ 
  content:""; 
  position:absolute; 
  left:0; 
  bottom:-1px; 
  height:1px; 
  width:0%; 
  background:currentColor; 
  transition:width .25s; 
}
.meta-link:hover::after{ width:100%; }
```

### Back Links
```css
.back-link {
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:11px; 
  color:var(--muted);
  text-transform:uppercase; 
  letter-spacing:1px; 
  text-decoration:none;
  margin-bottom:20px; 
  display:inline-block; 
  position:relative; 
  padding-bottom:2px;
}
.back-link::after{ 
  content:""; 
  position:absolute; 
  left:0; 
  bottom:-1px; 
  height:1px; 
  width:0%; 
  background:currentColor; 
  transition:width .25s; 
}
.back-link:hover::after{ width:100%; }
.back-link:hover{ color:var(--ink); }
```

## Content Patterns

### Dropcap (for article openings)
```css
.dropcap{
  float:left; 
  font-size:70px; 
  line-height:50px; 
  padding-top:8px; 
  padding-right:8px; 
  padding-left:3px;
  font-weight:400; 
  color:#000;
}
```

### Pullquotes
```css
.pullquote{
  font-size:24px; 
  font-style:italic; 
  color:#000; 
  margin:40px 60px; 
  padding:20px 0;
  border-top:1px solid #ddd; 
  border-bottom:1px solid #ddd; 
  text-align:center; 
  line-height:1.4;
}
```

### Author Bio
```css
.author-bio{
  margin-top:60px; 
  padding-top:30px; 
  border-top:1px solid #ddd;
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:14px; 
  color:#666; 
  line-height:1.5;
}
```

## Legal/Technical Content

### Legal Sections
```css
.legal-section {
  margin: 30px 0;
}

.legal-item {
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 15px;
}

.legal-list {
  margin-left: 20px;
}

.legal-list li {
  margin-bottom: 8px;
}
```

## SEO Footer Pattern

### Main Footer Structure
```css
.seo-footer {
  margin-top: 50px;
  padding-top: 30px;
  border-top: 2px solid var(--ink);
  text-align: center;
}

.seo-grid { 
  display:grid; 
  grid-template-columns:repeat(2,1fr); 
  gap:50px; 
  margin:0 0 30px 0; 
}

.seo-column-title {
  font-family:'IBM Plex Sans',sans-serif; 
  font-size:11px; 
  color:var(--muted); 
  letter-spacing:1px; 
  text-transform:uppercase; 
  margin:0 0 15px 0; 
  font-weight:500; 
  padding-bottom:8px; 
  border-bottom:1px solid var(--soft);
}

.seo-link {
  font-family:'Crimson Text',serif; 
  font-size:14px; 
  color:var(--ink); 
  text-decoration:none; 
  position:relative; 
  padding:2px 0; 
  transition:color .25s; 
  line-height:1.4;
}
.seo-link:hover { color: var(--muted); }
.seo-link::after { 
  content:''; 
  position:absolute; 
  left:0; 
  bottom:0; 
  width:0; 
  height:1px; 
  background-color:var(--muted); 
  transition:width .25s; 
}
.seo-link:hover::after { width:100%; }
```

## Responsive Breakpoints

```css
/* Mobile */
@media (max-width: 600px) {
  .magazine-title{ font-size:44px; letter-spacing:8px; }
  .seo-grid { grid-template-columns: 1fr; gap: 30px; }
}

/* Tablet */
@media (max-width: 768px) and (min-width: 601px) {
  .seo-grid { grid-template-columns: repeat(2, 1fr); gap: 35px; }
}
```

## Brand Guidelines

### Colors
- **Primary Background**: #fff1e5 (Financial Times salmon-pink)
- **Text**: #000 (pure black) and #2c2c2c (dark gray for body)
- **Secondary**: #666 (medium gray) and #777 (lighter gray for legal text)
- **Borders**: #ddd (light gray) and #dadada (CTA borders)

### Typography Rules
- **Headlines**: Always use Aboreto with uppercase and wide letter-spacing
- **Body**: Crimson Text, justified, with proper line-height (1.7)
- **UI Elements**: IBM Plex Sans, uppercase, with letter-spacing
- **Legal Text**: Smaller sizes (12px, 11px) but maintain readability

### CTA Box Rules
- **Primary CTAs**: Use `.case-box` with #dadada border (NEVER black)
- **Secondary CTAs**: Use `.cta-box` with #ddd border
- **Always center-aligned with proper padding (28px)**
- **Aboreto for titles, Crimson Text for descriptions**

### Content Structure
- **Always include**: Back link, masthead, article header, content, author bio
- **Section titles**: Uppercase, letter-spaced, IBM Plex Sans
- **Consistent spacing**: 40px margins, 20px between paragraphs
- **Hover effects**: Subtle underline animations on all links

### Page Types
- **Landing Page**: Includes dropcap, case boxes, pullquotes, SEO footer
- **Article Pages**: Standard article structure with back navigation
- **Legal Pages**: Formal structure with legal sections and proper formatting

This framework ensures pixel-perfect consistency across all CXO Resume materials while maintaining the sophisticated, editorial aesthetic appropriate for C-suite executives.
