# MONETEC SLIDE EXTRACTION INSTRUCTIONS

## Presentation URL
https://omnipresent.co.com/share/9Cqw5juW8Sbz

## Methods to Extract HTML

### Method 1: Browser Console Script
```javascript
// Run this in the browser console on each slide
let slideCount = 1;

function saveCurrentSlide() {
    const html = document.documentElement.outerHTML;
    const blob = new Blob([html], {type: 'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = `slide-${String(slideCount).padStart(2, '0')}.html`;
    a.click();
    URL.revokeObjectURL(url);
    console.log(`Saved slide ${slideCount}`);
    slideCount++;
}

// Save current slide
saveCurrentSlide();
```

### Method 2: Developer Tools
1. Open presentation
2. Press F12 for DevTools
3. Navigate to each slide
4. In Elements tab, find the slide container
5. Right-click > Copy > Copy outerHTML
6. Save to file

### Method 3: View Source
1. Navigate to slide
2. Right-click > View Page Source
3. Ctrl+A > Ctrl+C
4. Save to new HTML file

## File Naming Convention
- slide-01-hero.html ✅
- slide-02-comparison.html
- slide-03-triptych.html  
- slide-04-dashboard.html
- slide-05-map.html
- slide-06-transformation.html
- slide-07-cta.html

## Save Location
C:/Users/batis/Documents/MONETEC-PROJECT/06-HTML-SLIDES/

## Status
- Slide 1: ✅ Extracted and saved
- Slides 2-7: ⏳ Pending extraction