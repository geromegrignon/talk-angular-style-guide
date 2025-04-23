---
theme: seriph
background: https://images.unsplash.com/photo-1555066931-4365d14bab8c?q=80&w=2070&auto=format&fit=crop
title: 200 shades of angular style guide
info: |
  ## Angular Style Guide Evolution
  A presentation about the evolution of Angular style guide and recent changes.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# 200 shades of angular style guide

<div class="text-xl text-gray-500 mt-4">
  The evolution of Angular's style recommendations
</div>

<div @click="$slidev.nav.next" class="mt-12 py-1">
  Press Space for next page <carbon-arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/angular/angular" target="_blank" class="slidev-icon-btn">
    <carbon-logo-github />
  </a>
</div>

<!--
Welcome to this presentation about the evolution of Angular's style guide.
-->

---
transition: fade-out
---

# Abstract

One key argument for using Angular is the consistency it brings to your codebase and how it enforces it so switching from one project to another one is a breeze.

We are encouraged to write Angular application through 2 tools:

- the Angular CLI, shaping some inner responsabilities and boundaries within an Angular application
- the official style guide released back in Angular v2.

While some practices have evolved over time, this guide has remained unchanged.

However, both the web platform and the framework have evolved since then, and it was necessary for the style guide to evolve as well.

But as we create some habits, this new version might affect some of our practices.

Let's dive into the proposed changes and see how we can adapt to them.

<style>
h1 {
  background-color: #DD0031;
  background-image: linear-gradient(45deg, #DD0031 10%, #C3002F 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>

<!--
This abstract sets the stage for our discussion about the Angular style guide evolution.
-->

---
transition: slide-up
---

# The Original Angular Style Guide

The Angular Style Guide has been a cornerstone of Angular development since Angular 2.

<div class="grid grid-cols-2 gap-4">
<div>

## Purpose

- Provide consistency across Angular projects
- Establish best practices for Angular development
- Make it easier to onboard new developers
- Improve code maintainability and readability

</div>
<div>

## Key Principles

- Follow a consistent file and folder structure
- Use consistent naming conventions
- Follow a single responsibility principle
- Maintain proper encapsulation
- Optimize for readability

</div>
</div>

<!--
The Angular Style Guide has been a fundamental part of the Angular ecosystem since Angular 2. It has helped establish consistency across Angular projects and made it easier for developers to switch between different Angular codebases.
-->

---
layout: two-cols
layoutClass: gap-16
---

# Why Update the Style Guide?

After years of stability, the Angular team recognized the need to update the style guide to reflect modern practices.

<div class="mb-4">

## Evolving Ecosystem

- Angular has evolved significantly since Angular 2
- Modern JavaScript/TypeScript features are now widely used
- Web development best practices have changed
- Developer expectations have shifted

</div>

::right::

## Community Feedback

The community has been requesting updates to address:

- Outdated conventions
- Inconsistencies with modern Angular practices
- Better alignment with TypeScript best practices
- Support for newer Angular features
- Simplified file naming conventions

---
layout: default
---

# The GitHub Discussion

In October 2023, the Angular team started a [discussion](https://github.com/angular/angular/discussions/58412) about updating the style guide.

```md
# Angular Style Guide Update

The Angular Style Guide was first published in 2016 and has remained largely unchanged since then. 
However, both the web platform and the framework have evolved since then, and it's time for the 
style guide to evolve as well.
```

## Key Points from the Discussion

- The style guide hadn't been significantly updated since 2016
- Many conventions were outdated or inconsistent with modern practices
- The community was actively engaged, with over 100 comments
- Several specific areas were identified for improvement
- The team proposed a formal RFC process for the changes

<!--
The GitHub discussion was very active, showing that the community cares deeply about the style guide and has strong opinions about how it should evolve.
-->

---
layout: default
---

# The RFC: Proposed Changes

In February 2024, the Angular team published a [Request for Comments (RFC)](https://github.com/angular/angular/discussions/59522) with specific proposed changes to the style guide.

## Key Areas of Change

1. **File Naming Conventions**
   - Simplify file naming by removing the type suffix from most files
   - Example: `hero.component.ts` → `hero.ts`

2. **Directory Structure**
   - Organize by feature rather than by file type
   - Group related files together

3. **Component Selectors**
   - Use element selectors for components (e.g., `<app-hero>`)
   - Use attribute selectors for directives (e.g., `[appHighlight]`)

4. **Naming Conventions**
   - Use consistent naming patterns
   - Follow TypeScript conventions more closely

<!--
The RFC process allowed the community to provide structured feedback on the proposed changes before they were implemented.
-->

---
layout: two-cols
---

# File Naming Changes

The most significant and controversial change was the proposal to simplify file naming conventions.

## Current Convention

```
hero.component.ts
hero.component.html
hero.component.css
hero.service.ts
hero.module.ts
hero.pipe.ts
hero.directive.ts
```

:::right::

## Proposed Convention

```
hero.ts
hero.html
hero.css
hero.service.ts
hero.module.ts
hero.pipe.ts
hero.directive.ts
```

<div class="mt-8 text-sm">
<strong>Rationale:</strong> The Angular team argued that the type suffix is redundant in most cases:

- The file extension already indicates it's TypeScript
- The content of the file makes it clear it's a component
- IDEs can easily distinguish between different types of files
- Reduces verbosity and improves developer experience
</div>

<!--
The file naming changes generated the most discussion in the community, with strong opinions both for and against the changes.
-->

---
layout: default
---

# Community Reactions

The proposed changes generated significant discussion in the community, with mixed reactions.

<div class="grid grid-cols-2 gap-4">
<div>

## Arguments in Favor

- Simpler, less verbose file names
- More aligned with modern TypeScript practices
- Reduced cognitive load when working with files
- Better IDE integration with shorter names
- More flexibility for project organization

</div>
<div>

## Arguments Against

- Breaking years of established conventions
- Potential confusion during transition period
- Harder to distinguish file types at a glance
- Migration costs for existing projects
- Tooling and documentation updates needed

</div>
</div>

<div class="mt-4 text-center">
The community was particularly divided on the file naming changes, with many developers having strong preferences based on years of established habits.
</div>

<!--
The community discussion showed how deeply ingrained the Angular style guide had become in developers' workflows and habits.
-->

---
layout: default
---

# The Final Decision: PR #60809

In May 2024, the Angular team [merged a pull request](https://github.com/angular/angular/pull/60809) that updated the style guide based on the RFC and community feedback.

## The Compromise Solution

After considering all feedback, the Angular team decided to:

1. **Keep the component suffix for component files**
   - `hero.component.ts` remains the recommended format
   - This maintains backward compatibility with existing codebases

2. **Adopt other modernizations**
   - Updated directory structure recommendations
   - Improved naming conventions for services and other artifacts
   - Enhanced guidance for component organization

3. **Make the guide more flexible**
   - Acknowledge that teams may have established conventions
   - Provide rationale for recommendations rather than strict rules
   - Focus on consistency within a project

<!--
The final decision shows how the Angular team balanced innovation with stability, acknowledging the importance of established conventions while still moving the framework forward.
-->

---
layout: center
class: text-center
---

# Conclusion: Lessons from the Angular Style Guide Evolution

<div class="grid grid-cols-2 gap-8 mt-8">
<div class="text-left">

## Key Takeaways

- Style guides evolve as technologies and practices change
- Community feedback is essential for successful evolution
- Breaking changes require careful consideration
- Balancing innovation with stability is challenging
- Consistency within a project is more important than following external standards

</div>
<div class="text-left">

## What This Means for Angular Developers

- Be aware of the updated style guide recommendations
- Consider adopting new practices for new projects
- Maintain consistency within existing projects
- Understand the rationale behind the recommendations
- Participate in community discussions to shape future changes

</div>
</div>

<div class="mt-8 text-center text-gray-500">
The Angular style guide evolution demonstrates how a mature framework can adapt to changing practices while respecting its established community.
</div>

<!--
The Angular style guide evolution is a case study in how technical standards evolve in response to changing technologies and community needs.
-->

---
layout: center
class: text-center
---

# Thank You!

<div class="text-xl text-gray-500 mt-4 mb-8">
  For more information about the Angular style guide evolution:
</div>

<div class="grid grid-cols-3 gap-4">
  <div>
    <h3>Initial Discussion</h3>
    <a href="https://github.com/angular/angular/discussions/58412" target="_blank" class="text-blue-500">
      github.com/angular/angular/discussions/58412
    </a>
  </div>
  <div>
    <h3>RFC Explanation</h3>
    <a href="https://github.com/angular/angular/discussions/59522" target="_blank" class="text-blue-500">
      github.com/angular/angular/discussions/59522
    </a>
  </div>
  <div>
    <h3>Final Implementation</h3>
    <a href="https://github.com/angular/angular/pull/60809" target="_blank" class="text-blue-500">
      github.com/angular/angular/pull/60809
    </a>
  </div>
</div>

<div class="mt-12 text-sm text-gray-400">
  Presentation created with <a href="https://sli.dev" target="_blank" class="text-gray-400">Slidev</a>
</div>
