# 💎 UI/UX SUPERPOWER WORKFLOWS

## 21ST.DEV INTEGRATION

### API Configuration
```javascript
const API_KEY = "fb9bc23301c985525b3c81d007ba82ffe6a407431650f4dadef82020628523d7";
const USERNAME = "donruben";
const PLAN = "PRO_PLUS"; // Unlimited requests
```

### Quick Commands
- `/ui [description]` - Generate component
- `/21 [search]` - Find components
- `/logo [company]` - Get logos instantly
- `/refine [component]` - Improve existing UI

### Component Discovery Workflow

1. **Search Phase**
   ```javascript
   // Search for specific component types
   const searches = {
     hero: "dark hero animated logo",
     comparison: "split screen comparison",
     gallery: "triptych gallery modern",
     dashboard: "hexagonal dashboard data",
     map: "interactive map europe",
     transformation: "transformation animation",
     showcase: "real estate showcase"
   };
   ```

2. **Preview Phase**
   - Test components in isolation
   - Check responsiveness
   - Verify animations

3. **Implementation Phase**
   - Integrate with project
   - Apply brand colors
   - Add custom logic

### Design System Creation

```javascript
// Extract patterns from existing UI
const designSystem = {
  colors: {
    primary: "#F5A700",
    secondary: "#0A2647",
    background: "#000000"
  },
  typography: {
    heading: "Montserrat ExtraLight",
    body: "Montserrat Regular",
    numbers: "Montserrat Medium"
  },
  animations: {
    emergence: "fadeIn 1.5s ease-out",
    hover: "scale(1.05) transition 0.3s"
  }
};
```

### Rapid Prototyping

1. **Figma → Code**
   ```bash
   /figma extract [url]
   /21st convert --framework react
   /github push --branch prototype
   ```

2. **Component Library**
   ```bash
   /21st search "component type"
   /ui generate --style "brand guidelines"
   /refine --animation "hollywood"
   ```

### A/B Testing Workflow

```javascript
// Generate multiple versions
const versions = [
  { variant: "A", style: "minimal" },
  { variant: "B", style: "animated" },
  { variant: "C", style: "interactive" }
];

// Test each version
versions.forEach(v => {
  generateComponent(v);
  trackMetrics(v);
});
```