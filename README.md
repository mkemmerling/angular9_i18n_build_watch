# Angular 9/Ivy + i18n: Empty main.js.map when built in watch mode

## 🐞 bug report

### Affected Package

The issue is caused by Ivy.


### Is this a regression?

Yes, the previous version in which this bug was not present was: Angular 8


### Description

In Angular 9 when building a localized bundle in watch mode with, e.g., `ng build --configuration=de --watch` the created main.js.map SourceMap is just an empty object.

Not sure if this is a bug or just a missing feature, but I couldn't find any documentation about it.

When Ivy is disabled in tsconfig.json the SourceMap is built as expected. The problem also doesn't occur with `ng serve`.


## 🔬 Minimal Reproduction

LINK

This is just a minimal 'repro-app' with i18n configuration as described in the Angular docs.

To reproduce the error run `ng build --configuration=de --watch` and inspect the empty main.js.map SourceMap in dist/repro-app/de.


## 🌍  Your Environment

**Angular Version:**
<pre><code>
Angular CLI: 9.0.1
Node: 13.8.0
OS: darwin x64

Angular: 9.0.0
... animations, common, compiler, compiler-cli, core, forms
... language-service, localize, platform-browser
... platform-browser-dynamic, router
Ivy Workspace: Yes

Package                           Version
-----------------------------------------------------------
@angular-devkit/architect         0.900.1
@angular-devkit/build-angular     0.900.1
@angular-devkit/build-optimizer   0.900.1
@angular-devkit/build-webpack     0.900.1
@angular-devkit/core              9.0.1
@angular-devkit/schematics        9.0.1
@angular/cli                      9.0.1
@ngtools/webpack                  9.0.1
@schematics/angular               9.0.1
@schematics/update                0.900.1
rxjs                              6.5.4
typescript                        3.7.5
webpack                           4.41.2
</code></pre>
