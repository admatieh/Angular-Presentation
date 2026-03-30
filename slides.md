# Angular Presentation
A practical intro to Angular

---

## What you should know so far

- HTML
- JavaScript or TypeScript
- A bit of CSS
- Git
- Basic programming concepts
  - variables
  - loops
  - functions
  - conditionals

---

## What is Angular?

- A web application framework for building Single Page Applications (SPAs)
- Built and maintained by Google
- Has a huge community
- Ecosystem includes tools, libraries, and community resources
- `ng-cookbook` and similar resources help developers move faster

---

## Angular vs React

### Angular

- Is a framework
- Has a built-in CLI
- Includes tools and packages for small to medium apps
- Is opinionated
- Encourages better code style consistency across teams

---

## Angular vs React

### React

- Is a library
- Does not come with a built-in CLI in the same way Angular does
- Usually requires extra packages even for small apps
- Gives more flexibility, but also more setup decisions

---

## Myths about Angular

- It is hard to learn
- It changes too much on every update
- Angular is slow  
  Not really
- Angular has a huge bundle size

---

## Angular Core Concepts

- Components
- Services
- Directives
- Pipes
- Data binding
- Event handlers
- HTTP module
- Forms module
- Routing
- Animations
- Testing
- Building for production

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