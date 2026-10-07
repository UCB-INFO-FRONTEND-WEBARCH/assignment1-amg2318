# Assignment 1 Grading Feedback
## INFO 153A/253A Front-End Web Architecture - Fall 2026

**Student:** grantajia  
**Repository:** https://github.com/amg2318/assignment1-amg2318  
**Graded commit:** aa61934fe84d (2026-10-01)  
**Date:** 2026-10-06

---

## Overall Score: 99/100

| Component | Points |
|---|---|
| Header Specifications | 15/15 |
| Left Navigation Specifications | 15/15 |
| Main Content Specifications | 15/15 |
| General Layout | 15/15 |
| Best Practices Implementation | 39/40 |
| **Total** | **99/100** |

---

## Detailed Rubric Breakdown

### Header Specifications (15/15 points)

**Font Size (2/2):** meets the rubric line

**Colors (4/4):** meets the rubric line

**Icons (5/5):** meets the rubric line

**Quick Find Box (4/4):** meets the rubric line

### Left Navigation Specifications (15/15 points)

**Font Size (2/2):** meets the rubric line

**Colors (2/2):** meets the rubric line

**Icons (2/2):** meets the rubric line

**Responsive Hide (4/4):** meets the rubric line

**List Structure (5/5):** meets the rubric line

### Main Content Specifications (15/15 points)

**Font Size (2/2):** meets the rubric line

**Colors (3/3):** meets the rubric line

**List Implementation (5/5):** meets the rubric line

**Horizontal Rules (5/5):** meets the rubric line

### General Layout (15/15 points)

**Font Family (4/4):** meets the rubric line

**Layout Method (5/5):** meets the rubric line

**Section Widths (6/6):** meets the rubric line

### Best Practices Implementation (39/40 points)

**Semantic HTML5 (14/15):** The sidebar is a bare `<aside>` with no `<nav>` inside, so the navigation list is not marked up as navigation.  
  Evidence: `index.html:31`; `index.html:32`; `facts.desktop.sidebar.bareAside`

**External Stylesheet (5/5):** meets the rubric line

**Content/Presentation Separation (10/10):** No font, center, bgcolor, align, style attributes or `<br>` spacing runs; all styling lives in styles.css.

**Classes and IDs (10/10):** All classes and ids are descriptive (site-header, task-list, nav-items, current-tab), use one kebab-case convention, and no id is reused.

---

## Strengths

- All six provided icons are referenced from assets/ with relative paths and load correctly, and the nav icons sit in the sidebar list items.
- Layout is clean: a grid for the page and sidebar/main columns (styles.css:83-86, 221-225), flex for the header, and a 300px sidebar that fills the rest of the width with the main column to its right.
- Task checkboxes are custom CSS circles (styles.css:178-188) and a 1px border-bottom separates the tasks (styles.css:162-164).
- Consistent kebab-case naming and a well-commented stylesheet, with Roboto loaded via Google Fonts and declared in the CSS.

## Areas for Improvement

- Wrap the nav list in a <nav> element. Right now the sidebar is a bare <aside> (index.html:31), so the navigation has no navigation landmark.
- Fix the unclosed tag at index.html:15: `<div class="left-content"` is missing its `>`. The browser swallows the following `<button type="button" class="hamburger">` into the div's attributes, so the hamburger button element is never created (it is absent from facts.desktop.classes) and the .hamburger rule at styles.css:26 never applies. Validate your HTML to catch this.
- Feedback only: the spec asks for the placeholder "Quick find". Yours is "Quick Find", which is accepted here, but match the spec's wording exactly. The check icon also has alt="menu icon" (index.html:25); use alt text that describes it, and add lang="en" to <html>.
- Feedback only: the 30/5 counter, the border-bottom task separators and the rest of the layout work well. At 400px the page scrolls horizontally (facts.mobile400.hasHorizontalOverflow). This is not scored, but check the header's padding on small screens.
