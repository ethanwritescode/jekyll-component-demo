---
layout: default
title: Home
---

# Welcome to Component Library

A minimal component library built with Jekyll and Liquid includes, demonstrating variable widgets semantics.

## Hero Component

{% include components/hero.html
  title="Build Beautiful UIs"
  subtitle="With reusable Liquid components"
  background_color="#007bff"
  cta_label="View Components"
  cta_href="/components/"
  height="md"
%}

## Featured Components

<div class="grid mt-3">
  {% include components/card.html
    title="Button"
    description="Flexible button component with multiple variants and sizes."
    footer="<a href='/components/#button-component' class='btn btn-sm btn-outline'>Learn more</a>"
  %}

  {% include components/card.html
    title="Card"
    description="Versatile card component for displaying content with images and footers."
    footer="<a href='/components/#card-component' class='btn btn-sm btn-outline'>Learn more</a>"
  %}

  {% include components/card.html
    title="Hero"
    description="Large hero sections for page introductions with call-to-action buttons."
    footer="<a href='/components/#hero-component' class='btn btn-sm btn-outline'>Learn more</a>"
  %}
</div>

## Quick Start

### 1. Include a Button

```liquid
{% raw %}{% include components/button.html
  label="Click me"
  href="#"
  variant="primary"
%}{% endraw %}
```

### 2. Include a Card

```liquid
{% raw %}{% include components/card.html
  title="My Card"
  description="Card description"
  image="/path/to/image.jpg"
%}{% endraw %}
```

### 3. Include a Hero

```liquid
{% raw %}{% include components/hero.html
  title="Welcome"
  subtitle="Hero subtitle"
  background_color="#007bff"
%}{% endraw %}
```

## Variable Widgets Semantics

All components follow the **variable widgets semantics** pattern:

- **Explicit Variables**: All behavior is controlled through named variables
- **Predictable Defaults**: Optional variables have sensible defaults
- **Composable**: Components can include other components
- **Semantic HTML**: Clean, accessible markup
- **CSS-Ready**: Pre-built styles for immediate use

<div class="mt-3">
  {% include components/button.html
    label="View Full Documentation"
    href="/components/"
    variant="primary"
    size="lg"
  %}
</div>
