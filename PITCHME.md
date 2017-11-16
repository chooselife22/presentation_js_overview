# JavaScript
### Stand 2017

---

### Worum geht`s?

* JavaScript Web Development - Stand 2017 und davor
* ECMAscript - Es gibt doch einen Standard ... oder?
* Welche JS-Tools brauche ich überhaupt?
* Beispiel: Webpack

---

### JS entwickelt sich weiter

* Von Utility-Bibliotheken (lodash, underscore, sugar, uvm.) zu nativer Unterstützung
* JS-Müdigkeit: ständig neue Tools und Frameworks
  * Frameworks, Transpilers, Package Management, Task-runner

---

### Hot Topics

* Dirty Checking
  * Alle paar Millisekunden wird auf beiden Seiten auf Änderungen geprüft
* Shadow DOM, Virtual DOM Representation
* Aktuelle Frameworks gehen von MVC/MVVM/MVWHATEVER zu Web-Components
  * https://medium.com/this-dot-labs/building-modern-web-applications-in-2017-791d2ef2e341

---

### Web-Components

* Elemente mit HTML, CSS, JS
  * Der ganze Code in einem Element (<my-component>)
  * Scoped CSS
* Browser nicht 100%ig unterstützt
  * Polyfills
* https://blog.pusher.com/realtime-web-components/

---

### ECMAscript

> ECMAScript (or ES) is a trademarked scripting-language specification standardized by Ecma International in ECMA-262 and ISO/IEC 16262. It was created to standardize JavaScript, so as to foster multiple independent implementations.

---

### ES2015/ES6

* Vielzahl von Änderungen (mehr als 50 neue Features)
* z.B. Promises, let, Arrow functions, class

---

### ES2016/ES7

* Zwei neue Features
  * Array.protype.includes (check ob ein array ein object/primitive enthält)
    * Sollte eigentlich contains heißen
      * Aber MooTools hat bereits eine Methode mit dem gleichen Namen implementiert
      * Wegen Abwärtskompatibilität includes genannt
  * Exponatiation Operator ** (2 ** 8)

---

### ES Weiterentwicklung mit standardisiertem Prozess

* Wer entwickelt ECMAscript? -> [TC39 (Technical Committee 39)](http://www.ecma-international.org/memento/TC39.htm)
* Prozess eingeführt weil ES2015 zu viele Features hatte und zu unübersichtlich war
* Vier Stages (alles public, jeder kann einreichen)
  * Stage 0 (erste Idee) bis Stage 4 (von mehr als zwei Browsern implementiertes Feature) http://2ality.com/2015/11/tc39-process.html
* Features die im Januar in Stage 4 sind kommen in die neue Version von ECMAscript

---

### ES2017/ES8

* https://hackernoon.com/es8-was-released-and-here-are-its-main-new-features-ee9c394adf66
* Async functions, String padding, Object.values, Object.entries, Object.getOwnPropertyDescriptors, Trailing commas in function parameter lists and calls, Shared memory and atomics
* Browser Support https://kangax.github.io/compat-table/esnext/

---

### Browser Support ES6

<iframe src='http://kangax.github.io/compat-table/es6/' width="800" height="500">
---

### Browser Support ES7,ES8,ESNext

* ES7+ http://kangax.github.io/compat-table/es2016plus/
* ES Next (alles was im Prozess zu finden ist) http://kangax.github.io/compat-table/esnext/

---

### Transpilers

* compile-to-JS Sprachen
  * Machen aus Code der nicht in allen Browsern läuft Code der in allen Browsern läuft
* Anscheinend gehts nicht ohne
* Braucht man das?
  * Alle modernen Browsern haben fast 100% Support für ES6 Features
  * Hängt stark davon ob für welche Browser/Systeme man entwickelt
  * https://medium.freecodecamp.org/you-might-not-need-to-transpile-your-javascript-4d5e0a438ca
* CoffeeScript, TypeScript, Babel, Traceur

---


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

### Node

* Modulesystem ersetzt require.js, common.js, ...
* Modules in verschiedenen Formaten (da geschrieben als require.js module, common.js module, ... )
* Ziel: ES Modules in allen Browsern als Standard

---

### Webpack

---

### Progressive Web-Apps https://developers.google.com/web/progressive-web-apps/

* Load instantly (Service Workers)
* Add to Homescreen (Offline Support)
* Push Notifications'
* Secure (https)
* Fast (RAIL Performance Model)
* Responsive

* Ziel: Besser sein als native Anwendungen

---

### Zusammenfassung

* ECMAscript entwickelt sich hin zu Standards und Versionierungs-Prozessen
* Immer weniger externe libaries notwendig
* Explizites Bundling von externen libaries
* Nicht verrückt machen lassen von den vielen Tools
* Eigenes Toolkit finden
* Gespannt sein auf neue ES versionen
