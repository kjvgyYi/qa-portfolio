# UI Responsive
UI / Responsive Testing Results

**Date:** April 2026  
**Tester:** Hlib Klipko  
**Tool:** Chrome DevTools — Device Toolbar

---

## Test Objects

| Site | URL |
|------|-----|
| OpenCart Demo | https://demo.opencart.com |
| Wikipedia | https://www.wikipedia.org |
| Books to Scrape | https://books.toscrape.com |

---

## Viewports Tested

| Viewport | Size | Device Type |
|----------|------|-------------|
| Mobile | 360px | Smartphone |
| Desktop | 1280px | Desktop |

---

## Results

| ID | Site | Viewport | Element Tested | Result | Notes |
|----|------|----------|----------------|--------|-------|
| UI-001 | OpenCart | 360px | Navigation menu | ✅ Pass | Correctly collapses to mobile menu |
| UI-002 | OpenCart | 360px | Product cards | ✅ Pass | Stack correctly on mobile |
| UI-003 | OpenCart | 360px | Registration form | ✅ Pass | All fields visible and usable |
| UI-004 | OpenCart | 1280px | Full layout | ✅ Pass | No overflow or broken elements |
| UI-005 | Wikipedia | 360px | Search field | ✅ Pass | Displays correctly on mobile |
| UI-006 | Wikipedia | 360px | Article text | ✅ Pass | Text fits within screen bounds |
| UI-007 | Books to Scrape | 360px | Product cards | ✅ Pass | Cards stack correctly |
| UI-008 | Books to Scrape | 360px | Price and title text | ✅ Pass | No truncation or overflow |

---

## Observation

All three tested sites demonstrated solid responsive behaviour across
mobile (360px) and desktop (1280px) viewports. No critical UI bugs were
found. This confirms that modern demo sites follow responsive design
standards. Tablet viewport (768px) was unavailable in Chrome DevTools
for these test sessions.

---

## Bug Found During Registration Testing

During functional testing of OpenCart registration form a validation
UX bug was discovered — see **BUG-002** in `bug-reports/` folder.
The bug is related to form behaviour, not responsive layout.
