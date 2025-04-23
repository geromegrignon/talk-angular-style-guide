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

# Angular and Consistency

One key argument for using Angular is the consistency it brings to your codebase and how it enforces it so switching from one project to another one is a breeze.

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
Angular's consistency is one of its strongest selling points for enterprise applications.
-->

---
transition: slide-up
---

# Tools for Angular Development

We are encouraged to write Angular application through 2 tools:

- the Angular CLI, shaping some inner responsabilities and boundaries within an Angular application
- the official style guide released back in Angular v2.

While some practices have evolved over time, this guide has remained unchanged.

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
The Angular CLI and style guide have been the two pillars of Angular development practices.
-->

---
transition: slide-up
---

# Evolution of the Style Guide

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
This sets the stage for our discussion about the Angular style guide evolution.
-->

---
transition: slide-up
---

# The Original Angular Style Guide

The Angular Style Guide has been a cornerstone of Angular development since Angular 2.

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
The Angular Style Guide has been a fundamental part of the Angular ecosystem since Angular 2.
-->

---
transition: slide-up
---

# Purpose of the Style Guide

- Provide consistency across Angular projects
- Establish best practices for Angular development
- Make it easier to onboard new developers
- Improve code maintainability and readability

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
The purpose of the Angular Style Guide is to create a consistent development experience across projects.
-->

---
transition: slide-up
---

# Key Principles of the Style Guide

- Follow a consistent file and folder structure
- Use consistent naming conventions
- Follow a single responsibility principle
- Maintain proper encapsulation
- Optimize for readability

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
The key principles of the Angular Style Guide help developers create maintainable and readable code.
-->

---
transition: slide-up
---

# Why Update the Style Guide?

After years of stability, the Angular team recognized the need to update the style guide to reflect modern practices.

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
After many years without significant updates, the Angular team decided it was time to revisit the style guide.
-->

---
transition: slide-up
---

# Evolving Ecosystem

The web development landscape has changed significantly:

- Angular has evolved significantly since Angular 2
- Modern JavaScript/TypeScript features are now widely used
- Web development best practices have changed
- Developer expectations have shifted

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
The JavaScript ecosystem has evolved rapidly since the original style guide was created.
-->

---
transition: slide-up
---

# Community Feedback

The community has been requesting updates to address:

- Outdated conventions
- Inconsistencies with modern Angular practices
- Better alignment with TypeScript best practices
- Support for newer Angular features
- Simplified file naming conventions

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
The Angular community has been vocal about the need for updated style guidelines.
-->

---
transition: slide-up
---

# The GitHub Discussion

In October 2023, the Angular team started a [discussion](https://github.com/angular/angular/discussions/58412) about updating the style guide.

```md
# Angular Style Guide Update

The Angular Style Guide was first published in 2016 and has remained largely unchanged since then. 
However, both the web platform and the framework have evolved since then, and it's time for the 
style guide to evolve as well.
```

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
The Angular team initiated a public discussion to gather feedback on updating the style guide.
-->

---
transition: slide-up
---

# Key Points from the Discussion

- The style guide hadn't been significantly updated since 2016
- Many conventions were outdated or inconsistent with modern practices
- The community was actively engaged, with over 100 comments
- Several specific areas were identified for improvement
- The team proposed a formal RFC process for the changes

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
The GitHub discussion was very active, showing that the community cares deeply about the style guide and has strong opinions about how it should evolve.
-->

---
transition: slide-up
---

# The RFC: Proposed Changes

In February 2024, the Angular team published a [Request for Comments (RFC)](https://github.com/angular/angular/discussions/59522) with specific proposed changes to the style guide.

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
The RFC process allowed the community to provide structured feedback on the proposed changes before they were implemented.
-->

---
transition: slide-up
---

# File Naming Conventions

The first key area of proposed change:

- Simplify file naming by removing the type suffix from most files
- Example: `hero.component.ts` → `hero.ts`

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
File naming conventions were one of the most significant proposed changes in the RFC.
-->

---
transition: slide-up
---

# Directory Structure

The second key area of proposed change:

- Organize by feature rather than by file type
- Group related files together

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
The proposed directory structure changes aimed to make Angular applications more modular and feature-focused.
-->

---
transition: slide-up
---

# Component Selectors

The third key area of proposed change:

- Use element selectors for components (e.g., `<app-hero>`)
- Use attribute selectors for directives (e.g., `[appHighlight]`)

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
The selector conventions help distinguish between components and directives in Angular templates.
-->

---
transition: slide-up
---

# Naming Conventions

The fourth key area of proposed change:

- Use consistent naming patterns
- Follow TypeScript conventions more closely

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
The naming convention changes aimed to align Angular more closely with modern TypeScript practices.
-->

---
transition: slide-up
---

# File Naming Changes

The most significant and controversial change was the proposal to simplify file naming conventions.

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
File naming was the most debated aspect of the proposed style guide changes.
-->

---
transition: slide-up
---

# Previous File Naming Convention

The original Angular naming pattern (used from Angular 2 until 2024):

```
hero.component.ts
hero.component.html
hero.component.css
hero.service.ts
hero.module.ts
hero.pipe.ts
hero.directive.ts
```

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
This convention was used since Angular 2 and became deeply ingrained in the community, but has now been replaced.
-->

---
transition: slide-up
---

# Current File Naming Convention

The new official Angular naming pattern (adopted in 2024):

```
user-profile.ts
user-profile.html
user-profile.css
user-profile.service.ts
user-profile.pipe.ts
user-profile.directive.ts
```

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
The current convention removes the component suffix from component files, simplifying file names.
-->

---
transition: slide-up
---

# Official File Naming Guidelines

The Angular style guide now provides clear rules for file naming:

- **Separate words with hyphens** (e.g., `user-profile.ts`)
- **Match file names to the TypeScript identifier** within the file
- **Use the same name for related files** (TypeScript, HTML, CSS)
- **Use `.spec.ts` suffix for test files** (e.g., `user-profile.spec.ts`)

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
The official style guide now provides clear and consistent rules for file naming that align with modern TypeScript practices.
-->

---
transition: slide-up
---

# Community Reactions

The proposed changes generated significant discussion in the community, with mixed reactions.

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
The community had strong and diverse opinions about the proposed style guide changes.
-->

---
transition: slide-up
---

# Arguments in Favor

Many developers supported the changes for these reasons:

- Simpler, less verbose file names
- More aligned with modern TypeScript practices
- Reduced cognitive load when working with files
- Better IDE integration with shorter names
- More flexibility for project organization

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
Supporters of the changes emphasized simplicity and alignment with modern practices.
-->

---
transition: slide-up
---

# Arguments Against

Other developers opposed the changes for these reasons:

- Breaking years of established conventions
- Potential confusion during transition period
- Harder to distinguish file types at a glance
- Migration costs for existing projects
- Tooling and documentation updates needed

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
Opponents of the changes were concerned about breaking established conventions and the costs of transition.
-->

---
transition: slide-up
---

# Community Division

The community was particularly divided on the file naming changes, with many developers having strong preferences based on years of established habits.

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
The community discussion showed how deeply ingrained the Angular style guide had become in developers' workflows and habits.
-->

---
transition: slide-up
---

# The Final Decision: PR #60809

In May 2024, the Angular team [merged a pull request](https://github.com/angular/angular/pull/60809) that updated the style guide based on the RFC and community feedback.

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
After months of discussion and feedback, the Angular team made their final decision on the style guide updates.
-->

---
transition: slide-up
---

# Removing Component Suffixes

The first aspect of the final solution:

- **Remove the component suffix from component files**
- `user-profile.ts` is now the recommended format instead of `user-profile.component.ts`
- This simplifies file naming and aligns with modern TypeScript practices

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
The Angular team ultimately decided to adopt the simplified file naming convention, removing type suffixes from component files.
-->

---
transition: slide-up
---

# Key Modernizations in the Style Guide

The second aspect of the final solution:

- **Feature-based project organization** instead of type-based directories
- **Prefer the `inject` function** over constructor parameter injection
- **Use `protected` for template-only members** and `readonly` for Angular-initialized properties
- **Prefer `class` and `style` bindings** over NgClass and NgStyle directives

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
The updated style guide includes several modern practices that align with current Angular and TypeScript best practices.
-->

---
transition: slide-up
---

# Emphasizing Consistency Within Projects

The third aspect of the final solution:

- **"When in doubt, prefer consistency"** is a key principle
- Prioritize maintaining consistency within a file over following external rules
- Provide clear rationale for each recommendation
- Focus on practices that promote maintainability and readability

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
The style guide emphasizes that consistency within a project is more important than rigidly following external standards, while still providing clear recommendations.
-->

---
transition: slide-up
---

# Conclusion: Lessons from the Angular Style Guide Evolution

The Angular style guide evolution demonstrates how a mature framework can adapt to changing practices while respecting its established community.

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
The Angular style guide evolution offers important lessons for framework maintainers and the developer community.
-->

---
transition: slide-up
---

# Key Takeaways

Important lessons from the style guide evolution process:

- Style guides evolve as technologies and practices change
- Community feedback is essential for successful evolution
- Breaking changes require careful consideration
- Balancing innovation with stability is challenging
- Consistency within a project is more important than following external standards

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
These key takeaways highlight the challenges and considerations in evolving technical standards.
-->

---
transition: slide-up
---

# What This Means for Angular Developers

Practical implications for developers working with Angular:

- **Adopt simplified file naming** for new projects (e.g., `user-profile.ts` instead of `user-profile.component.ts`)
- **Use the `inject()` function** instead of constructor parameter injection
- **Organize by feature** rather than by file type (avoid directories like "components" or "services")
- **Prioritize consistency** within your project over rigidly following external standards
- **Consider migrating** existing projects gradually, starting with new code

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
The updated style guide provides clear, practical guidance that developers can apply to improve their Angular projects.
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
