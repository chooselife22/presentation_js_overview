### Ziel des Vortrags

* Überblick Javascript
* ECMAscript
* Versionierung

## State of JS 2016

* https://www.youtube.com/watch?v=5NIL3Epadj0
* Jack Franklin treats us to his talk on 'The State of JavaScript', where he explores, discusses and criticises the current state of web development with JavaScript.

### Content

* More and more APIs
* Working in the browser without libaries

### NodeJS

* BOOMING
* exposing a lot more people to javascript
* Browsers building native support for library-features (document.querySelectorAll, =>, ...)
  * Features make it back into the language

### Two-Way-Data Binding (Example)

* Dirty Checking (done by frameworks) (every few (milli)seconds checking for updates on both sides)
  * Not performant, dirty ...
* We need something native
  * Object.observe

### Framework Competition
Example Virtual-DOM-Implementation
* React
* Ember -> Glimmer
* Angular
* Everyone has something like it

### Moving from MVC/MVVM/MVWHATEVER to Components

* https://medium.com/this-dot-labs/building-modern-web-applications-in-2017-791d2ef2e341
* Angular 1.5 moved heavily to Components
* Ember 2 removed controllers
* React only has Components

### Web-Components

* Elements with HTML, CSS, JS
  * All Code in one "Element"
  * Scoped CSS
* Browser-Support "Patchy"
  * Polyfills to fill the Gaps
* https://blog.pusher.com/realtime-web-components/

### ES2015/ES6

* Feature-heavy mess
* Tons of new features +50
* no one had a clue whats going on
* Some Features are cool
  * Promises
  * let
  * Arrow functions
  * class
* some not
  * const not "can not cange"
    * const is just a binding

### ES2016/ES7

* 2 Features
  * Array.protype.includes (check if array includes object/primitive)
    * Should be called contains...
      * But MooTools allready implemented a method with this name LoL (Backwards Compatibility)
  * Exponatiation Operator** (2 ** 8)

### Process for Accepting new feautures

* Who designs ECMAscript? -> TC39 (Technical Committee 39)
  * http://www.ecma-international.org/memento/TC39.htm

* anyone can propose a feature
* process introduced because ES2015 was to feature-heavy
* features goes through stages (tc39 process) happens on github (all public)
  * http://2ality.com/2015/11/tc39-process.html

* Every year in january, every feature that is in the last stage (two browser have to implement the feature) will be in the next version of ECMAscript

### ES2017/ES8

*

### Transpilers

* Babel
  * Taken the world by storm :D Unavoidable
  * Let us take code that doesnt run in all browsers and builds code that run in all browsers
* Do we need Transpilers?
  * All Browsers have more than 90% Support for ES2015 features
  * But Answer depends on Target (Multiple Browsers or only one)
  * https://medium.freecodecamp.org/you-might-not-need-to-transpile-your-javascript-4d5e0a438ca
* https://kangax.github.io/compat-table/es6/

### Node

* Modulesystem ersetzt require.js, common.js, ...
* Modules in verschiedenen Formaten (da geschrieben als require.js module, common.js module, ... )
* Ziel: ES Modules in allen Browsern als Standard

### ES Modules

* Angstrebter Standard
* Modules sind static (können nicht dynamisch geladen werden )
* Gezielte Imports (Tree Shaking -> alle toten Blätter fallen runter)

```
// Ohne Modules

Import:
import _ from 'lodash';

Verwenden:
_.map(...);

Includiert im komprimierten JS:
* Eigener JS-Code
* Alles von lodash

```

```
// Mit Modules

Import:
import map from 'lodash';

Verwenden:
map(...);

Includiert im komprimierten JS:

* Eigener JS-Code
* **Nur** map von lodash

```
* https://rollupjs.org/ -> Bundle für ES Modules

### Tooling

* JS-Fatigue: ständig neue Tools und Frameworks -> es ist hart mitzuhalten
* Frameworks: ...
* Package Management: Browserfy, Webpack, JSPM
* Transpilers: Babel, Traceur
* Task-runner: gulp, grunt, ...

### Progressive Web-Apps https://developers.google.com/web/progressive-web-apps/

* Load instantly (Service Workers)
* Add to Homescreen (Offline Support)
* Push Notifications'
* Secure (https)
* Fast (RAIL Performance Model)
* Responsive

* Ziel: Besser sein als native Anwendungen

### Zusammenfassung

* ECMAscript entwickelt sich hin zu Standards und Versionierungs-Prozessen
* Immer weniger externe libaries notwendig
* Explizites Bundling von externen libaries
* Nicht verrückt machen lassen von den vielen Tools
* Eigenes Toolkit finden
* Gespannt sein auf neue ES versionen

