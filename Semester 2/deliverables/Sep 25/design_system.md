# Design System & Component Library

## What You Need to Deliver

A documented component library for your web app with reusable UI components, design tokens, and clear usage guidelines. Think of it as your own mini-Bootstrap tailored specifically for your product.

## Key Questions

- Do you have consistent styling across your entire app?
- Can you quickly build new features using existing components?
- Is your design system easy for others to understand and use?

## What You Need to Submit

### Component Library
- [ ] **Live component showcase** (HTML page or Storybook)
- [ ] **GitHub repository** with organized component files
- [ ] **CSS/SCSS files** with design tokens and component styles
- [ ] **Component documentation** showing all states and variations

### Documentation
- [ ] **README.md** with setup instructions and component overview
- [ ] **Component docs** for each element (usage, states, code examples)

### Demo
- [ ] **5-minute video** showing your design system in action

## How to Get Started

### 1. Audit Your Current Design
Review your existing app and identify:
- Repeated UI elements (buttons, forms, cards, etc.)
- Inconsistent styling patterns
- Colors, fonts, and spacing being used

### 2. Define Design Tokens
Create foundational variables for:
- **Colors:** Primary, secondary, success, error, neutral
- **Typography:** Font families, sizes, weights
- **Spacing:** Margins, padding, gaps (8px, 16px, 24px, etc.)
- **Borders:** Radius, width, style

### 3. Build Core Components
Start with essentials (5-8 components):
- Button (primary, secondary, disabled states)
- Input fields (text, email, password, error states)
- Card/container
- Navigation elements
- Basic layout components

### 4. Document Everything
For each component, provide:
- Visual examples of all states
- HTML/CSS code snippets
- Usage guidelines (when to use, when not to use)
- Accessibility considerations

## Design System Structure

```
design-system/
├── README.md
├── index.html (component showcase)
├── css/
│   ├── tokens.css (design variables)
│   ├── base.css (reset, typography)
│   └── components/
│       ├── button.css
│       ├── form.css
│       ├── card.css
│       └── navigation.css
├── components/
│   ├── button/
│   │   ├── button.html
│   │   ├── button.css
│   │   └── README.md
│   └── form/
│       ├── form.html
│       ├── form.css
│       └── README.md
└── examples/
    └── page-samples.html
```

## Design Tokens Example

```css
/* tokens.css */
:root {
  /* Colors */
  --color-primary: #007bff;
  --color-primary-hover: #0056b3;
  --color-secondary: #6c757d;
  --color-success: #28a745;
  --color-error: #dc3545;
  --color-text: #212529;
  --color-text-muted: #6c757d;
  
  /* Typography */
  --font-family-base: 'Inter', sans-serif;
  --font-size-sm: 0.875rem;
  --font-size-base: 1rem;
  --font-size-lg: 1.25rem;
  --font-weight-normal: 400;
  --font-weight-bold: 600;
  
  /* Spacing */
  --spacing-xs: 0.5rem;
  --spacing-sm: 1rem;
  --spacing-md: 1.5rem;
  --spacing-lg: 2rem;
  
  /* Borders */
  --border-radius: 0.375rem;
  --border-width: 1px;
}
```

## Component Documentation Template

```markdown
# Button Component

## Overview
Primary action button used for main user actions like "Sign Up", "Save", "Submit".

## Usage
```html
<button class="btn btn-primary">Primary Action</button>
<button class="btn btn-secondary">Secondary Action</button>
<button class="btn btn-primary" disabled>Disabled</button>
```

## States
- Default: Standard appearance
- Hover: Darker background on mouse over
- Active: Pressed state appearance  
- Disabled: Grayed out, not clickable

## CSS
```css
.btn {
  padding: var(--spacing-xs) var(--spacing-sm);
  font-family: var(--font-family-base);
  font-weight: var(--font-weight-bold);
  border: none;
  border-radius: var(--border-radius);
  cursor: pointer;
}

.btn-primary {
  background-color: var(--color-primary);
  color: white;
}

.btn-primary:hover {
  background-color: var(--color-primary-hover);
}
```

## When to Use
- Primary actions (one per page/section)
- Form submissions
- Important user actions



## Success Criteria

- Can someone else use your design system without asking questions?
- Are your components consistent with your design_v2?
- Does your design system make your app look more professional?

## Resources

### Tools
- **CSS Frameworks:** Study Bootstrap, Tailwind CSS for inspiration
- **Documentation:** Use Storybook, or simple HTML pages
- **CSS Preprocessors:** SASS/SCSS for better organization
- **Design Tools:** Figma for designing component states

### Component Libraries to Study
- **Material-UI:** Google's Material Design components
- **Ant Design:** Enterprise-class UI components
- **Chakra UI:** Simple, modular components
- **Pure.css:** Minimal CSS framework

### Design Token Resources
- **CSS Custom Properties:** For design variables
- **Design Token Spec:** W3C Community Group specification
- **Style Dictionary:** Build system for design tokens

## Grading Rubric

| Criteria | Excellent (4) | Good (3) | Satisfactory (2) | Needs Work (1) |
|----------|---------------|----------|------------------|----------------|
| **Component Quality** | 5+ well-designed components with all states | 3-4 solid components with main states | Basic components that work | Poor or incomplete components |
| **Design Tokens** | Comprehensive token system used throughout | Good token usage with minor gaps | Basic tokens implemented | No consistent token usage |
| **Documentation** | Clear docs with examples and usage guidelines | Good documentation with minor gaps | Basic documentation | Poor or missing documentation |
| **Implementation** | Clean, organized code following best practices | Good code organization | Basic working code | Poor code quality or organization |
| **Consistency** | Perfect consistency across all components | Good consistency with minor deviations | Mostly consistent | Inconsistent or conflicting styles |

**Remember:** A good design system makes building UI faster and more consistent. Focus on the components you actually use in your app.
