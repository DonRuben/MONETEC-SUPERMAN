# 💻 21ST.DEV API CONFIGURATION

## AUTHENTICATION

```javascript
// API Credentials
const config = {
  apiKey: "fb9bc23301c985525b3c81d007ba82ffe6a407431650f4dadef82020628523d7",
  username: "donruben",
  plan: "PRO_PLUS",
  baseUrl: "https://api.21st.dev/v1"
};

// Headers for all requests
const headers = {
  'Authorization': `Bearer ${config.apiKey}`,
  'Content-Type': 'application/json',
  'X-User': config.username
};
```

## SEARCH ENDPOINTS

### Component Search
```javascript
// Search for components
async function searchComponents(query) {
  const response = await fetch(`${config.baseUrl}/search`, {
    method: 'POST',
    headers,
    body: JSON.stringify({
      query,
      filters: {
        framework: 'react',
        style: 'modern',
        hasAnimation: true
      }
    })
  });
  return response.json();
}
```

### Logo Search
```javascript
// Search for company logos
async function searchLogos(companies) {
  const response = await fetch(`${config.baseUrl}/logos`, {
    method: 'POST',
    headers,
    body: JSON.stringify({
      queries: companies,
      format: 'TSX'
    })
  });
  return response.json();
}
```

## COMPONENT GENERATION

### Generate UI Component
```javascript
// Generate new component
async function generateComponent(description) {
  const response = await fetch(`${config.baseUrl}/generate`, {
    method: 'POST',
    headers,
    body: JSON.stringify({
      prompt: description,
      framework: 'react',
      styling: 'tailwind',
      typescript: true
    })
  });
  return response.json();
}
```

### Refine Existing Component
```javascript
// Improve component
async function refineComponent(code, improvements) {
  const response = await fetch(`${config.baseUrl}/refine`, {
    method: 'POST',
    headers,
    body: JSON.stringify({
      code,
      context: improvements,
      preserveLogic: true
    })
  });
  return response.json();
}
```

## MONETEC SEARCHES

```javascript
// Pre-configured searches for each slide
const monetecSearches = {
  slide1: {
    query: "dark hero section animated logo hexagonal",
    filters: { hasAnimation: true, theme: "dark" }
  },
  slide2: {
    query: "split screen comparison layout",
    filters: { layout: "split", responsive: true }
  },
  slide3: {
    query: "three column triptych gallery modern",
    filters: { columns: 3, style: "minimal" }
  },
  slide4: {
    query: "hexagonal dashboard data visualization",
    filters: { shape: "hexagon", interactive: true }
  },
  slide5: {
    query: "interactive map europe pins animation",
    filters: { region: "europe", animated: true }
  },
  slide6: {
    query: "before after transformation morphing",
    filters: { transition: "morph", comparison: true }
  },
  slide7: {
    query: "contact cta real estate premium",
    filters: { purpose: "cta", industry: "real-estate" }
  }
};
```

## IMPLEMENTATION WORKFLOW

```javascript
// Complete workflow for Monetec
async function implementMonetecSlides() {
  const results = {};
  
  // Search for each slide
  for (const [slide, config] of Object.entries(monetecSearches)) {
    results[slide] = await searchComponents(config.query);
  }
  
  // Apply brand colors
  const brandedComponents = applyBrandColors(results, {
    primary: '#F5A700',
    secondary: '#0A2647',
    background: '#000000'
  });
  
  return brandedComponents;
}
```