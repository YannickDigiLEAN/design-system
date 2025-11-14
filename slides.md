---
theme: default
title: Design System
class: text-center
---

# Design System

for the next generation web client

---

# What's a Design System ?

What it is.

- concerns applications *"Look & Feel"*
- is a set of guidelines, rules, patterns, ...
- gets agreed upon and then followed during development

## Benefits

- Users: provide cohesive user experience across whole app
- Mangement: lessen decision making & reduce technical debt
- Developers: simplify & accelerate development workflow

## Goal

*Maintain a style guide, available to the whole team, that defines in detail how things should look.*

---
layout: two-cols
---

# What's a Design System ?

What it contains.

::left::

## Design tokens

*Atomic style variables, ie.*

- typography (font family, weights, headlines, ...)
- colors (accent, secondary, error, success, ...)
- spacing (margins, paddings, gaps, ...)
- icons (icon set, semantics)

::right::

## Components

*Interactive & form elements, ie.*

- buttons
- text inputs
- checkboxes, radios
- dropdowns, selects
- calendars
- charts
- ... and thousands more

---
layout: three-cols
---

# Adopting a Design System

Using existing solutions or creating new.

::left::

## *Prebuilt*

<span class="text-neutral-400">Use existing</span>

<div class="text-sm">

- Pick fitting UI/component framework
- Adjust colors, fonts & minor tweaks

<ul>
<li class="plus">Little additional work</li>
<li class="plus">Cohesive look & feel</li>
<li class="plus">Loads of stable components</li>
<li class="minus">Generic appearance</li>
<li class="minus">Very dependent on 3rd party</li>
</ul>
</div>
::center::

## *Hybrid*

<span class="text-neutral-400">Modify existing</span>

<div class="text-sm">

- Pick fitting UI/component framework
- Define design tokens
- Reset & override styles
<ul>
<li class="plus">Unique brand design</li>
<li class="plus">Loads of stable components</li>
<li class="minus">Maintenance & migrating</li>
<li class="minus">Dependent on 3rd party</li>
</ul>
</div>

::right::

## *From scratch*

<span class="text-neutral-400">Create new</span>

<div class="text-sm">

- Define design tokens
- Style native HTML elements

<ul>
<li class="plus">Fully independent</li>
<li class="plus">Unique brand design</li>
<li class="minus">Lots of work</li>
<li class="minus">Complex components are big pain</li>
<li class="minus">Pitfalls: responsiveness, accessability, polyfills</li>
</ul>

</div>

<style>
    ul {
      list-style: none;
      padding-left: 0;
    }

    li {
      position: relative;
      padding-left: 1.8rem;
      margin-bottom: 0.4rem;

        &::before {
            content: "■";
            position: absolute;
            left: 0.15rem;
            top: 0.1rem;
            font-size: 0.4rem;
            color: #d4cfbf;
        }
        
        &.plus {
            color: oklch(79.2% 0.209 151.711);
            &::before {
                content: "+";
                color: oklch(79.2% 0.209 151.711);
                font-weight: bold;
                font-size: 1rem;
                left: 0;
            }
            
        }

        &.minus {
            color: oklch(70.4% 0.191 22.216);
            &::before {
                content: "−";
                color: oklch(70.4% 0.191 22.216);
                font-weight: bold;
                font-size: 1rem;
                left: 0;
            }
        }
    }
</style>

---

# Picking a UI library

What to look out for.

- *Pricing model:* Are all components available or are some paywalled?
- *Customization:* How easy can styles be adjusted & overriden?
- *Dependencies:* Is the library itself depending on other 3rd party libraries?
- *Templates:* Does the library offer prebuilt UI blocks?
- *UI kits:* Does the library offer style definition files (eg. Figma, Adobe XD, ...)?


Obvious other concerns are stability, adoption among big players, history, similarity to current design, ...

---

# UI libraries

## *PrimeReact*

<br>

- By *PrimeFaces*
- Also available for *Angular* & *Vue*
- Well suited for style reset & customization

<br>

<div class="flex justify-end">
<img class="rounded-xl opacity-85" width="55%" src="https://www.primefaces.org/wp-content/uploads/2021/12/primereact-release-7.jpeg" />
</div>

---

# UI libraries

## *shadcn*

<br>

- By *Vercel*
- Uses *TailwindCSS* and wraps around *Radix UI* components
- Uses local components (they live inside the project)

<br>

<div class="flex justify-end">
<img class="rounded-xl opacity-85" width="50%" src="https://s3-alpha.figma.com/hub/file/5052349927/559314a0-c97f-4ac1-b82c-b456ce626bd0-cover.png" />
</div>

---

# UI libraries

## *WebAwesome*

<br>

- By *FontAwesome* creators
- Tightly follows web standards
- Framework agnostic

<br>

<div class="flex justify-end">
<img class="rounded-xl opacity-85" width="60%" src="./assets/webawesome.png" />
</div>

---

# UI libraries

## *Material UI*

<br>

- Seems quite popular
- Extensive customization/theming options
- Considerable paywalls

<br>

<div class="flex justify-end">
<img class="rounded-xl opacity-85" width="55%" src="./assets/material-ui.png" />
</div>

---

# Not a UI library

## *TailwindCSS*

<br>

- CSS utility framework
- Not a component library
- No distinct look or style

<br>

<div class="flex justify-end">
<img class="rounded-xl opacity-85" width="55%" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Frepository-images.githubusercontent.com%2F130268121%2Fb4fd5300-b585-11ea-8718-1e141e78842e&f=1&nofb=1&ipt=c9c8e84fef6d2d988fefa9d4dc8051c2810592e66d0681d9c7bc57c1665562a3" />
</div>

---

# External Web designer

Considering outside expertise.

## Potential issues

- How to transport the current look and feel to new client?
- How to adopt UI framework style to our needs and style?
- How to create/maintain a style definition document?

## A Web designer could...

- ... take into account the current applications design
- ... use a UI frameworks style kit as a base
- ... condense both into a fresh/rebranded brand style
- and create a *standardized style guide* as reference for developers.

---

# Decisions, decisions...

What the next steps could be.

<div class="text-center">
```mermaid {scale: 0.55}
graph TB
A[Choose approach]
B[Pick UI/component library]
C[Want external design expertise?]
D[Receive style guide/ Figma kit]
E[Define design tokens]
F[Create styled components]

A -->|Prebuilt| B
A -->|Hybrid| B
A -->|From scratch| C
B --> C
C -->|yes| D
C -->|no| E
D --> E
E --> F
```
</div>