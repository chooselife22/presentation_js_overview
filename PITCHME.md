# JavaScript
### Stand 2017

---

### Worum geht`s?

* JavaScript Web Development - bis heute
* ECMAscript - Es gibt doch einen Standard ... oder?
* JavaScript-Toolchain (Beispiel: Webpack)

---

## JavaScript Web Development
*Übersicht*

---

### JS entwickelt sich weiter

* Von Utility-Bibliotheken (jQuery, lodash, underscore, uvm.) zu nativer Unterstützung
* JS-Müdigkeit: Frameworks, Transpilers, Package Management, Task-runner, ...

---

### Hot Topics

* ES6/ES7/ESNext
* Shadow/Virtual DOM, async/await und promises, ES modules
* MVC/MVVM/MVWHATEVER zu Web-Components
* Native zu Progressive Web-Apps

---

### Web-Components

* Elemente mit HTML, CSS, JS
* Verwendung des Shadow-DOM (Scoped CSS)
* Browser nicht 100%ig unterstützt (Polyfills)

---

### Progressive Web-Apps

* Müssen über HTTPS laufen
* Manifest File - Metainformationen und installierbar auf Homescreen
* Offline arbeiten - Inhalte lokal cachen (Service Workers)
* Push Notifications
* Performant (RAIL Performance Model von Google)
* Responsive für gängige Größen
* **Ziel:** Native Anwendungen ablösen

---

## ECMAscript

> ECMAScript (or ES) is a trademarked scripting-language specification standardized by Ecma International in ECMA-262 and ISO/IEC 16262. It was created to standardize JavaScript, so as to foster multiple independent implementations.

---

### ECMAscript Releases

* Weil ES2015 zur viele Features
* Entwickelt von [TC39 (Technical Committee 39)](http://www.ecma-international.org/memento/TC39.htm)
* [Release Prozess](http://2ality.com/2015/11/tc39-process.html) mit Vier Stages
  * Stage 0 (erste Idee)
  * ...
  * Stage 4 (von mehr als zwei Browsern implementiertes Feature)
  * Alles public GitHub
* Stage 4 Features kommen im Januar in neue Version

---

## ES2015/ES6

* Default Parameters, Template Literals, Multi-line Strings, Destructuring Assignment, Enhanced Object Literals, Arrow Functions, Promises, Block-Scoped Constructs Let and Const, Classes, Modules
* https://webapplog.com/es6/
* Browser Support: http://kangax.github.io/compat-table/es6/

---

### ES2016/ES7

* **2** neue Features
* *Array.protype.includes* (check ob ein array ein object/primitive enthält)
  * Sollte *contains* heißen
  * Aber MooTools hat bereits Methode mit gleichen Namen
  * Wegen Abwärtskompatibilität *includes* genannt
* Exponential Operator \**

---

### ES2017/ES8

* Async functions, String padding, Object.values, Object.entries, Object.getOwnPropertyDescriptors, Trailing commas in function parameter lists and calls, Shared memory and atomics
* https://hackernoon.com/es8-was-released-and-here-are-its-main-new-features-ee9c394adf66

---


### Browser Support ES7, ES8, ESNext

* ES7+ http://kangax.github.io/compat-table/es2016plus/
* ES Next (alles was im Prozess zu finden ist) http://kangax.github.io/compat-table/esnext/

---

## JS-Toolchain
*Brauch ich das wirklich ... alles?*

---

### Transpilers

* compile-to-JS Sprachen
  * Machen aus Code der nicht in allen Browsern läuft Code der in allen Browsern läuft
* Anscheinend gehts nicht ohne
* Braucht man das?
  * Alle modernen Browsern haben fast 100% Support für ES6 Features
  * Hängt stark davon ob für welche Browser/Systeme man entwickelt
* CoffeeScript, TypeScript, Babel, Traceur


---

### Package Management
*ohne Modules*

```
import _ from 'lodash';

Verwenden:
_.map(...);

Includiert im komprimierten JS:
* Eigener JS-Code
* Alles von lodash

```

---

### Package Management
*mit Modules*


```
import map from 'lodash';

Verwenden:
map(...);

Includiert im komprimierten JS:

* Eigener JS-Code
* **Nur** map von lodash

```

---

### Modulsyntax ist verschieden

* Node (CommonJS Module Format) https://nodejs.org/docs/latest/api/modules.html
* require.js (define, require) http://requirejs.org/docs/api.html#jsfiles

---

### ES Modules

* Einheitlicher Standard

```
//------ lib.js ------
export const sqrt = Math.sqrt;
export function square(x) {
    return x * x;
}
export function diag(x, y) {
    return sqrt(square(x) + square(y));
}

//------ main.js ------
import { square, diag } from 'lib';
console.log(square(11)); // 121
console.log(diag(4, 3)); // 5
```

* http://exploringjs.com/es6/ch_modules.html#sec_basics-of-es6-modules

---

### Webpack

* Implementiert ES Modules

---

### Webpack & Rails

* webpacker Gem
* http://www.stefanwienert.de/blog/2017/05/20/rails-webpacker-vue-js/

---

## Zusammenfassung

* Releaseprozess ECMAscript
* Weniger externe Bibliotheken mehr native Funktionen
* Eigenes Toolkit finden
* Gespannt sein auf neue ES versionen (und selbst submitten :D)

---

## Links

* RAIL Performance Model - https://developers.google.com/web/fundamentals/performance/rail
* Progressive Web Apps - https://medium.com/this-dot-labs/building-modern-web-applications-in-2017-791d2ef2e341
* Web Components - https://blog.pusher.com/realtime-web-components/
* Transpilers - https://developers.google.com/web/fundamentals/performance/rail
* ES6 Features - https://webapplog.com/es6/
* ES6 Compatibility - http://es6-features.org/#Constants
