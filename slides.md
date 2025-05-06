---
theme: seriph
background: /backgrounds/primary-bg.png
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

<h1 class="font-[BungeeHairline]">
200 shades of 
<img src="/icons/angular-logo.svg" class="inline-block w-16 h-16" />
<span class="font-[BungeeInline] text-pink-500">angular</span>
style guide
</h1>

<div class="text-xl text-gray-400 mt-4">
  The evolution of Angular's style recommendations
</div>

<!--
Welcome to this presentation about the evolution of Angular's style guide.
-->


---
layout: image
image: /images/gitdiff.png
backgroundSize: 20em
---

---
layout: image-left

# the image source
image: /images/coding-style-guide-viewer.png

# a custom class name to the content
class: my-cool-content-on-the-right
---

<h1 class="font-[BungeeInline] !text-pink-500">Angular coding style guide</h1>

<v-click>

Looking for an opinionated guide to Angular syntax, conventions, and application structure? Step right in. This style guide presents preferred conventions and, as importantly, explains why.

</v-click>

<v-clicks>

- Provide consistency across Angular projects
- Establish best practices for Angular development
- Make it easier to onboard new developers
- Improve code maintainability and readability

</v-clicks>

---
layout: quote
---

<v-click at="+1">

Style Guides require experience building applications with the tools. My style guide for Angular 1 was based on years of experience with Angular 1, collaboration with other Angular experts, and conributions from the Angular core team.

</v-click>

<v-click at="0">

Nobody has the same massive experience with Angular 2, and thus the Angular 2 Style Guide is a work in progress.

</v-click>


---
layout: image
image: /images/john-papa.png
---

---
transition: slide-up
---

<h1 class="font-[BungeeInline] text-pink-500">Angular style guide RFC</h1>

<v-clicks> 

- Make the style guide shorter. The current style guide is 52 (!) pages when printed.
- Simplify guidance that was overly cumbersome or boilerplate-y
- Remove most guidance that doesn't meaningfully relate to Angular
- Focus the style guide more on style choices rather than general Angular best practices
- Modernize guidance to reflect new features and APIs in the framework
- Update prior recommendations based on our observations of Angular development in the real world

</v-clicks> 

<!--
Introducing the Angular RFC as a way to understand the motivation to talk about Anfgular style guide, not just a momentum but part ofa bigger and official process.
-->


---
transition: slide-up
layout: section
---

<h1 class="font-[BungeeInline] !text-white"><span class="!text-pink-500">Angular</span> Renaissance</h1>

<!--
Angular Renaissance is the name given to the period of time where Angular has been evolving a lot.
If used for Angular 17 release which saw the logo and docs changes, it happened a few versions before, when Angular introduced Standalone API, paving the way for a whole new way of writing Angular applications.

The RFC however not hapenned with Angular 17 released but after Angular 19 one.
This RFC goal was to reconsider totally the way we write Angular applications and how we can improve it.
As the style guide stayed unchanged for years, it was a good opportunity to revisit it globally.
-->

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">1.</h2>
<h1 class="font-[BungeeInline] !text-white">Standards</h1>
<h2 class="font-[BungeeInline] !text-pink-500">VS</h2>
<h1 class="font-[BungeeInline] !text-white">best practices</h1>


<!--
The style guide is not a best practices list, it's a set of recommendations that are there to help you write Angular applications.
It's not a list of do's and don'ts, but a set of recommendations to help you write Angular applications.

Not following the style guide does not make you a bad developer, it just means you have your own style.
But as the current style guide is quite famous, not following it makes your project harder to maintain and harder to understand for newcomers.

Not following best practices is another story: it's about impacting performance, security, maintainability, readability and more.

A good way to sum up the differences is to say that the style guide is about "how to write Angular code", while best practices are about "how to write good code". Best practices are more related to the API and the framework, while the style guide is more about the code organization and the readability  .
-->

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">2.</h2>
<h1 class="font-[BungeeInline] !text-white"><span class="!text-pink-500">Angular</span> only</h1>


---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">2.</h2>
<h1 class="font-[BungeeInline] !text-white">no more<span class="!text-pink-500"> suffixes</span></h1>


```
user-profile.component.ts and UserProfileComponent
user-profile.component.ts and UserProfileComponent
```

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">3.</h2>
<h1 class="font-[BungeeInline] !text-white">get rid of<span class="!text-pink-500"> NGMODULES</span></h1>


<v-click>

```
ng generate @angular/core:standalone
```

</v-click>



---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">4.</h2>
<h1 class="font-[BungeeInline] !text-white">Template</h1>
<h2 class="font-[BungeeInline] !text-pink-500">VS</h2>
<h1 class="font-[BungeeInline] !text-white">templatesurl</h1>

---
layout: two-cols
---

# TemplateURL

```ts
@Component({
  selector: 'app-hero',
  standalone: true,
  templateUrl: './hero.component.html',
  styleUrls: ['./hero.component.css'],
}))
export class HeroComponent {}
```

::right::

# Template

```ts
@Component({
  selector: 'app-hero',
  standalone: true,
  template: `
    <h1>Hero</h1>
    <p>Hero works!</p>
  `,
  styles: [`
    h1 {
      color: red;
    }
  `],
}))
export class HeroComponent {}
```

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">5.</h2>
<h1 class="font-[BungeeInline] !text-white">say yes</h1>
<h2 class="font-[BungeeInline] !text-pink-500">to</h2>
<h1 class="font-[BungeeInline] !text-white">HOST & CLASS</h1>

---
transition: slide-up
lyout: section
---

```ts
@Component({
  ...,
  host: {
    'role': 'slider',
    '[attr.aria-valuenow]': 'value',
    '[class.active]': 'isActive()',
    '[tabIndex]': 'disabled ? -1 : 0',
    '(keydown)': 'updateValue($event)',
  },
})
export class CustomSlider {
  value: number = 0;
  disabled: boolean = false;
  isActive = signal(false);
  updateValue(event: KeyboardEvent) { /* ... */ }
  /* ... */
}
```

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">6.</h2>
<h1 class="font-[BungeeInline] !text-white">say no</h1>
<h2 class="font-[BungeeInline] !text-pink-500">to</h2>
<h1 class="font-[BungeeInline] !text-white">onClick</h1>


---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">7.</h2>
<h2 class="font-[BungeeInline] !text-white">what about</h2>
<h1 class="font-[BungeeInline] !text-pink-500">signals</h1>

---
transition: slide-up
layout: image
image: /images/caniuse.png
---


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
---

<h1 class="font-[BungeeInline] !text-pink-500">Resources</h1>

- [John Papa Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a2/notes.md)

- [Angular Style Guide RFC](https://github.com/angular/angular/discussions/58412)
- [Angular Style Guide Summary](https://github.com/angular/angular/discussions/59522)

- [Former Angular style guide](https://github.com/angular/angular/blob/64cfe18dbc833f1e54fceb5090c4b97538cdd9a4/adev/src/content/best-practices/style-guide.md)
- [New Angular style guide](https://github.com/angular/angular/blob/main/adev/src/content/best-practices/style-guide.md)


---
layout: two-cols
---

<img src="/images/qr-code.png" class="w-50 h-50" />

::right::

<h2 class="font-[BungeeInline] !text-pink-500">GEROME GRIGNON</h2>

- Angular Devs France leader
- NG Baguette Conf co-organizer
- Angular Discord Admin
- Angular Can I Use creator
