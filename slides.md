# Angular Framework
A practical intro to the framework for modern web apps

---

## What you should know so far

<div class="two-col checklist-slide">
  <div class="card soft-card">
  
  ### Web Basics
  - HTML & CSS
  - JavaScript
  - Basics of modern JS (ES6)
  
  </div>

  <div class="concept-box">
  
  ### Programming Concepts
  - Variables & Data Types
  - Functions & Scope
  - Conditionals & Loops
  - Classes & Objects
  
  </div>
</div>

---

## What is Angular?

<div class="content-narrow">

- A platform and framework for building Single Page Applications (SPAs).
- Built and maintained by Google.
- Solves the problem of structuring and scaling complex web applications.
- Commonly used in enterprise environments, large-scale projects, and teams that need a reliable, structured foundation.

</div>

---

## Why use Angular?

<div class="two-col">
  <div class="card">
  
  ### Developer Experience
  - **TypeScript:** Built-in strong typing for fewer bugs.
  - **Angular CLI:** Powerful command-line tool to generate code and manage builds.
  - **Opinionated Structure:** Clear patterns so teams don't have to invent their own architecture.
  
  </div>

  <div class="card">
  
  ### Batteries Included
  - **Routing:** Built-in tools for navigating between views.
  - **Forms:** Robust handling for complex user inputs.
  - **HTTP:** Built-in client to talk to APIs quickly.
  - **Scalability:** Designed to grow from a small app to massive codebases.
  
  </div>
</div>

---

## How Angular Apps Are Built

<div class="section-lead">A beginner-friendly mental model.</div>

<div class="content-narrow">

Think of your app as a tree of Lego blocks. The pieces snap together to form the whole UI.

- **Components:** The actual Lego blocks. Each is a specific piece of UI (like a header, a button, or a user card).
- **Templates:** The blueprint for how that specific Lego block looks (HTML).
- **Services:** Delivery trucks that carry data (like fetching a user list from a server) to giving it to the Lego blocks.

</div>

---

## Core Concepts Overview

<div class="section-lead">The essential pieces you'll use every day.</div>

--

## Components

<div class="two-col">
  <div>

Components are the fundamental building blocks of an Angular application. They control a patch of screen (a view).

- Every app has at least one (the root component).
- They connect a TypeScript class containing logic with an HTML template that renders the UI.

  </div>
  <div>

**Example:**
```typescript
@Component({
  selector: 'app-hello',
  template: '<h1>Hello, {{ name }}!</h1>',
  styles: ['h1 { color: blue; }']
})
export class HelloComponent {
  name = 'Angular';
}
```

  </div>
</div>

--

## Templates & Data Binding

<div class="two-col">
  <div>

Data binding seamlessly connects your component's data to what the user sees on the screen.

- **Interpolation:** `{{ value }}` - Puts data directly into text.
- **Property Binding:** `[property]="value"` - Sets HTML attributes dynamically.
- **Two-Way Binding:** `[(ngModel)]="value"` - Keeps data and inputs perfectly synced.

  </div>
  <div>

**Example:**
```html
<!-- Interpolation -->
<h1>Welcome, {{ user.name }}</h1>

<!-- Property Binding -->
<button [disabled]="isFormInvalid">Submit</button>

<!-- Two-Way Binding -->
<input [(ngModel)]="username">
<p>You typed: {{ username }}</p>
```

  </div>
</div>

--

## Event Binding

<div class="two-col">
  <div>

Event binding lets your app respond to user actions like keystrokes, mouse clicks, and touches.

- Syntax: `(eventName)="methodName()"`
- It listens for the event on the DOM and triggers a method inside your component's TypeScript class.

  </div>
  <div>

**Example:**
```html
<!-- Click Event -->
<button (click)="saveData()">Save</button>

<!-- Keyboard Event -->
<input (keyup.enter)="submitForm()">
```

```typescript
export class DemoComponent {
  saveData() {
    alert('Data saved successfully!');
  }
}
```

  </div>
</div>

--

## Directives

<div class="two-col">
  <div>

Directives tell Angular how to manipulate the DOM (the HTML structure).

- **Structural Directives:** Add or remove elements from the page entirely (`*ngIf`, `*ngFor`).
- **Attribute Directives:** Change the appearance or behavior of a single element (`[ngClass]`, `[ngStyle]`).

  </div>
  <div>

**Example:**
```html
<!-- Structural Directives -->
<div *ngIf="isLoggedIn">
  Welcome back!
</div>

<ul>
  <li *ngFor="let item of list">{{ item }}</li>
</ul>

<!-- Attribute Directive -->
<p [ngClass]="{'active': isActive}">
  Highlight me
</p>
```

  </div>
</div>

--

## Pipes

<div class="two-col">
  <div>

Pipes take in raw data as input and transform it into a formatted string right inside the template.

- They don't change the underlying data, just how it displays.
- Built-in pipes include `DatePipe`, `UpperCasePipe`, and `CurrencyPipe`.
- You can chain them using the `|` symbol.

  </div>
  <div>

**Example:**
```html
<!-- Transforms "angular" to "ANGULAR" -->
<p>{{ 'angular' | uppercase }}</p>

<!-- Formats a raw date object -->
<p>{{ today | date:'mediumDate' }}</p>

<!-- Formats a number to currency ($1,234.50) -->
<p>{{ price | currency:'USD' }}</p>
```

  </div>
</div>

--

## Services & DI

<div class="two-col">
  <div>

**Services** are shared helpers. Instead of copying logic into 5 different components, you write it once in a service.

**Dependency Injection (DI)** is Angular's way of automatically delivering these services. If your component needs a `DataService`, DI hands it one automatically.

  </div>
  <div>

**Example:**
```typescript
@Injectable({ providedIn: 'root' })
export class DataService {
  getUsers() { return ['Alice', 'Bob']; }
}

@Component({...})
export class UserList {
  // Angular injects the service here!
  constructor(private dataService: DataService) {}
  
  users = this.dataService.getUsers();
}
```

  </div>
</div>

---

## Common Built-In Features

<div class="two-col">
  <div class="card soft-card">
    <h3>Routing & Navigation</h3>
    <p>Angular handles moving between pages without refreshing the browser using the `@angular/router` package.</p>
  </div>

  <div class="card soft-card">
    <h3>Forms</h3>
    <p>Provides powerful tools for validating input and tracking form state (Reactive Forms & Template-Driven Forms).</p>
  </div>
</div>

<div class="two-col" style="margin-top: 1rem;">
  <div class="card soft-card">
    <h3>HTTP Client</h3>
    <p>A built-in module to easily make API requests to servers and handle responses safely.</p>
  </div>

  <div class="card soft-card">
    <h3>Testing</h3>
    <p>Apps generate with pre-configured unit and integration testing tools right out of the box.</p>
  </div>
</div>

---

## Creating an Angular app

<div class="content-narrow">

```bash
# 1. Install the Angular CLI globally
npm install -g @angular/cli

# 2. Check that it worked
ng version

# 3. Create a brand new application
ng new my-awesome-app

# 4. Navigate in and start the server
cd my-awesome-app
ng serve --open
```

</div>

---

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
    <h3>React (Library)</h3>
    <ul>
      <li><strong>Focused on UI:</strong> Only handles displaying components. You choose your own routing and HTTP packages.</li>
      <li>Highly flexible: Teams can structure code however they want.</li>
      <li>Easier to start, harder to master perfectly.</li>
      <li>Uses JavaScript or TypeScript.</li>
    </ul>
  </div>
</div>

---

## Common Misconceptions

<div class="content-narrow text-left">

**"Angular is too hard to learn."**
It takes time, but it pays off. You are learning universal software concepts that make you a better overall developer.

**"Angular is slow and bloated."**
Modern Angular is incredibly fast. Tools like standalone components and new change detection mechanisms make it smaller and faster than ever.

**"It changes too much."**
While updating used to be painful years ago, the Angular team now provides automated update commands (`ng update`) that heavily reduce friction.

</div>

---

## Summary & Next Steps

<div class="two-col">
  <div class="card soft-card">
  
  ### Summary
  - Angular is a structured, powerful framework.
  - Apps are built by composing **Components**.
  - **Templates** handle UI, **Services** handle business logic.
  - **Directives** and **Pipes** make manipulating screens easy.
  
  </div>

  <div class="concept-box">
  
  ### Next Steps
  1. Install the tools: Node.js and VS Code.
  2. Install `@angular/cli`.
  3. Run `ng new first-app` and explore the `src/app` folder.
  4. Edit `app.component.html` and watch the browser update!
  
  </div>
</div>

