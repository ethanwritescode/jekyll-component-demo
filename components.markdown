---
layout: page
title: Component Library
permalink: /components/
---

# Component Library

A minimal component library built with Liquid includes and variable widgets semantics.

---

## Button Component

The button component supports multiple variants and sizes.

### Usage

```liquid
{% raw %}{% include components/button.html
  label="Click me"
  href="/page"
  variant="primary"
  size="md"
%}{% endraw %}
```

### Examples

**Primary Button:**
{% include components/button.html label="Primary Button" href="#" variant="primary" %}

**Secondary Button:**
{% include components/button.html label="Secondary Button" href="#" variant="secondary" %}

**Outline Button:**
{% include components/button.html label="Outline Button" href="#" variant="outline" %}

**Different Sizes:**

Small: {% include components/button.html label="Small" href="#" size="sm" %}
Medium: {% include components/button.html label="Medium" href="#" size="md" %}
Large: {% include components/button.html label="Large" href="#" size="lg" %}

**Disabled Button:**
{% include components/button.html label="Disabled" href="#" disabled=true %}

### Variables

| Variable | Type | Default | Required | Description |
|----------|------|---------|----------|-------------|
| `label` | string | — | ✓ | Button text |
| `href` | string | — | ✗ | Link destination (creates `<a>` if provided, else `<button>`) |
| `variant` | string | "primary" | ✗ | "primary", "secondary", or "outline" |
| `size` | string | "md" | ✗ | "sm", "md", or "lg" |
| `disabled` | boolean | false | ✗ | Disable the button |
| `class` | string | — | ✗ | Additional CSS classes |

---

## Card Component

Cards display content with optional images, titles, and footers.

### Usage

```liquid
{% raw %}{% include components/card.html
  title="Card Title"
  description="Card description"
  image="/image.jpg"
  footer="Footer content"
%}{% endraw %}
```

### Examples

**Simple Card:**
{% include components/card.html
  title="Simple Card"
  description="This is a simple card with title and description."
%}

**Card with Image:**
{% include components/card.html
  title="Card with Image"
  description="This card has an image and description."
  image="https://via.placeholder.com/300x200?text=Card+Image"
%}

**Card with Footer:**
{% include components/card.html
  title="Card with Footer"
  description="This card has a footer with action buttons."
  footer='<button class="btn btn-primary btn-sm">Learn More</button>'
%}

### Variables

| Variable | Type | Default | Required | Description |
|----------|------|---------|----------|-------------|
| `title` | string | — | ✗ | Card title |
| `description` | string | — | ✗ | Card description |
| `image` | string | — | ✗ | Image URL |
| `footer` | string | — | ✗ | Footer content (can include HTML) |
| `class` | string | — | ✗ | Additional CSS classes |

---

## Hero Component

Large hero sections for page introductions with optional call-to-action.

### Usage

```liquid
{% raw %}{% include components/hero.html
  title="Welcome"
  subtitle="This is a hero section"
  background_color="#007bff"
  cta_label="Get Started"
  cta_href="/page"
  height="lg"
%}{% endraw %}
```

### Examples

**Basic Hero:**
{% include components/hero.html
  title="Welcome to Our Site"
  subtitle="Build amazing things with our component library"
  background_color="#007bff"
%}

**Hero with CTA:**
{% include components/hero.html
  title="Get Started Today"
  subtitle="Join thousands of users creating beautiful experiences"
  background_color="#28a745"
  cta_label="Start Now"
  cta_href="/components"
  height="md"
%}

**Hero with Background Image:**
{% include components/hero.html
  title="Background Hero"
  subtitle="Heroes can have background images"
  background_image="https://via.placeholder.com/1200x400?text=Hero+Background"
  background_color="rgba(0,0,0,0.5)"
  cta_label="Learn More"
  cta_href="#"
  height="lg"
%}

### Variables

| Variable | Type | Default | Required | Description |
|----------|------|---------|----------|-------------|
| `title` | string | — | ✓ | Hero title |
| `subtitle` | string | — | ✗ | Hero subtitle |
| `background_image` | string | — | ✗ | Background image URL |
| `background_color` | string | "#f5f5f5" | ✗ | Background color |
| `cta_label` | string | — | ✗ | Call-to-action button text |
| `cta_href` | string | — | ✗ | Call-to-action link |
| `height` | string | "lg" | ✗ | "sm", "md", or "lg" |
| `class` | string | — | ✗ | Additional CSS classes |

---

## Variable Widgets Semantics

These components follow variable widgets semantics:

- **Variables as Properties**: All component behavior is controlled via Liquid variables passed as `include` parameters
- **Composition**: Components can include other components (e.g., Hero includes Button)
- **Flexible Content**: Some components support optional content blocks
- **Defaults**: Smart defaults for all optional variables
- **CSS Classes**: Components use semantic class names for styling

This pattern allows for maximum flexibility and composability while maintaining clean, simple component interfaces.
