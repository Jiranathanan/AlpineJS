# Alpine JS is an amazing tool.
# 📘 Alpine.js Basic Documentation

> A lightweight JavaScript framework for adding interactivity to your HTML using declarative syntax, similar to Vue.js, but smaller and more minimal.

---

## 🔧 Installation

You can include Alpine.js in your project using a CDN:

```html
<script src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js" defer></script>
```

Or install via npm:

```bash
npm install alpinejs
```

Then import it in your JS:
```javascript
import Alpine from 'alpinejs'
window.Alpine = Alpine
Alpine.start()
```

#📦 Basic Syntax
x-data
Defines Alpine component state.

```html
<div x-data="{ count: 0 }">
  <button @click="count++">Increment</button>
  <span x-text="count"></span>
</div>
```

x-init
Runs JavaScript code when a component is initialized.
```html
<div x-data="{ message: '' }" x-init="message = 'Hello, Alpine!'">
  <span x-text="message"></span>
</div>
```

x-show
Conditionally show/hide elements.
```html
<div x-data="{ open: false }">
  <button @click="open = !open">Toggle</button>
  <div x-show="open">Hello!</div>
</div>
```
x-bind
Bind HTML attributes dynamically.
```html
<div x-data="{ color: 'red' }">
  <input x-bind:style="'color: ' + color" />
</div>
```
x-on / @
Add event listeners.
```html
<button x-on:click="count++">Click</button>
<!-- Shortcut -->
<button @click="count++">Click</button>
```

#🧠 Common Use Cases
Toggle Dropdown
```html
<div x-data="{ open: false }">
  <button @click="open = !open">Menu</button>
  <ul x-show="open">
    <li>Profile</li>
    <li>Settings</li>
  </ul>
</div>
```

Form Handling
```html
<form x-data="{ name: '' }" @submit.prevent="alert(name)">
  <input type="text" x-model="name" placeholder="Enter name" />
  <button type="submit">Submit</button>
</form>
```





