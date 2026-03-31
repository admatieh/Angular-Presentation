# Angular Framework
A practical intro to Angular

---

## What you should know so far

<div class="two-col checklist-slide">
  <div class="card soft-card">

  - HTML
  - JavaScript or TypeScript
  - A bit of CSS
  - Git

  </div>

  <div class="concept-box">

  ### Basic programming concepts

  - Variables
  - Loops
  - Functions
  - Conditionals

  </div>
</div>

---

## What is Angular?

<div class="content-narrow">

- A web application framework for building Single Page Applications (SPAs)
- Built and maintained by Google
- Has a huge community
- Includes tools, libraries, and community resources
- `ng-cookbook` and similar resources help developers move faster

</div>

---
## Angular vs React

<div class="section-lead">Two popular approaches, different philosophies.</div>

--

## Angular vs React

<div class="compare-grid">
  <div class="compare-card">
    <h3>Angular</h3>
    <ul>
      <li><strong>Is a framework</strong></li>
      <li>Has a built-in CLI</li>
      <li>Includes tools and packages for small to medium apps</li>
      <li>Is opinionated</li>
      <li>Encourages better code style consistency across teams</li>
    </ul>
  </div>

  <div class="compare-card">
    <h3>React</h3>
    <ul>
      <li><strong>Is a library</strong></li>
      <li>Does not come with a built-in CLI in the same way Angular does</li>
      <li>Usually requires extra packages even for small apps</li>
      <li>Gives more flexibility, but also more setup decisions</li>
    </ul>
  </div>
</div>
---

## Myths about Angular

<div class="content-narrow">

- It is hard to learn
- It changes too much on every update
- Angular is slow (<a href="https://krausest.github.io/js-framework-benchmark/2024/table_chrome_129.0.6668.58.html" target="_blank" class="inline-link">Not really</a>)
- Angular has a huge bundle size

</div>

---
## Angular Core Concepts

<div class="section-lead">The building blocks you use every day.</div>

--

## Angular Core Concepts

<div class="two-col">
  <div class="card">
    <h3>The Basics</h3>
    <ul>
      <li>Components</li>
      <li>Services</li>
      <li>Directives</li>
      <li>Pipes</li>
      <li>Data binding</li>
      <li>Event handlers</li>
    </ul>
  </div>

  <div class="card">
    <h3>Advanced Features</h3>
    <ul>
      <li>HTTP module</li>
      <li>Forms module</li>
      <li>Routing</li>
      <li>Animations</li>
      <li>Testing</li>
      <li>Building for production</li>
    </ul>
  </div>
</div>
---

## Creating an Angular app

```bash
# install the Angular CLI
npm install -g @angular/cli

# check CLI version
ng --version

# create an app
ng new first-ng-app

# optionally preview without creating files
ng new first-ng-app --dry-run

# create an app with some configuration
ng new first-ng-app --inline-style --inline-template