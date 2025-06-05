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

<h1 class="font-[BungeeInline] !text-white"><span class="!text-pink-500">Angular</span> style guide RFC</h1>

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

<h2 class="font-[BungeeInline] !text-pink-500">3.</h2>
<h1 class="font-[BungeeInline] !text-white">no more<span class="!text-pink-500"> suffixes</span></h1>

<v-click>

```
user-profile.component.ts to user-profile.ts
UserProfileComponent to UserProfile
```

</v-click>

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">4.</h2>
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

<h2 class="font-[BungeeInline] !text-pink-500">5.</h2>
<h1 class="font-[BungeeInline] !text-white">Template</h1>
<h2 class="font-[BungeeInline] !text-pink-500">VS</h2>
<h1 class="font-[BungeeInline] !text-white">templatesurl</h1>

---
layout: two-cols
---

# TemplateURL

<div class="m-2">

```ts
@Component({
  selector: 'app-hero',
  templateUrl: './hero.html',
  styleUrls: ['./hero.css'],
}))
export class Hero {}
```

</div>

::right::

# Template

<div class="m-2">

```ts
@Component({
  selector: 'app-hero',
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
export class Hero {}
```

</div>

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">6.</h2>
<h1 class="font-[BungeeInline] !text-white">say yes</h1>
<h2 class="font-[BungeeInline] !text-pink-500">to</h2>
<h1 class="font-[BungeeInline] !text-white">HOST & CLASS</h1>

---
transition: slide-up
lyout: section
---

```ts {1-3,8-14|4-5|6|7}
@Component({
  ...,
  host: {
    'role': 'slider',
    '[attr.aria-valuenow]': 'value',
    '[class.active]': 'isActive()',
    '(keydown)': 'updateValue($event)',
  },
})
export class CustomSlider {
  value: number = 0;
  disabled: boolean = false;
  isActive = signal(false);
  updateValue(event: KeyboardEvent) { /* ... */ }
}
```

---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">7.</h2>
<h1 class="font-[BungeeInline] !text-white">say no</h1>
<h2 class="font-[BungeeInline] !text-pink-500">to</h2>
<h1 class="font-[BungeeInline] !text-white">onClick</h1>

---
layout: two-cols
---

# TemplateURL

<div class="m-2">

```ts
@Component({
    selector: 'app-hero',
    template: `
    <button (click)="onButtonClick()">Save</button>
  `,
    styles: [`
    h1 {
      color: red;
    }
  `],
}))
export class Hero {
    onButtonClick() {
        // handle button click
    }
}
```

</div>

::right::

# Template

<div class="m-2">

```ts
@Component({
  selector: 'app-hero',
  template: `
    <button (click)="save()">Save</button>
  `,
}))
export class Hero {
    save() {
        // handle button click
    }
}
```

</div>



---
transition: slide-up
layout: section
---

<h2 class="font-[BungeeInline] !text-pink-500">8.</h2>
<h2 class="font-[BungeeInline] !text-white">what about</h2>
<h1 class="font-[BungeeInline] !text-pink-500">signals</h1>

---
transition: slide-up
layout: image
image: /images/caniuse.png
---

---
transition: slide-up
layout: section
---

<h1 class="font-[BungeeInline] !text-pink-500">RFC <span class="!text-white">SUMMARY</span></h1>
<h3 class="font-[BungeeInline]">April 2025</h3>


---
transition: slide-up
layout: section
---

<h3 class="font-[BungeeInline]">Goodbye</h3>
<h1 class="font-[BungeeInline] !text-pink-500">.ng <span class="!text-white">files</span></h1>

<v-click>

```
user-profile.component.ts => user-profile.ng.ts => user-profile.ts
```

</v-click>


---
transition: slide-up
layout: center
---

```ts
// user-profile.ts
@Component({
    selector: 'app-user-profile',
    templateUrl: './user-profile.html',
    styleUrls: ['./user-profile.css'],
})
export class UserProfile {}
```

---
transition: slide-up
layout: section
---

<h1 class="font-[BungeeInline] !text-pink-500">inject <span class="!text-white">function</span></h1>

<v-click>

```ts
private userApi = inject(UserApi);
```

</v-click>


---
transition: slide-up
---

<h1 class="font-[BungeeInline] !text-pink-500">KEEP <span class="!text-white">it</span></h1>


<v-clicks>

- consistency
- folder structure
- file naming (including specs)
- create within src folder
- bootstrap with main.ts
- keep component simples
- protected and readonly recommandations

</v-clicks>

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

<h2 class="font-[BungeeInline] !text-pink-500 mb-20">GEROME GRIGNON</h2>

- Angular Devs France leader
- NG Baguette Conf co-organizer
- Angular Discord Admin
- Angular Can I Use creator
