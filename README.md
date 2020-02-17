## StartTag
Repo to reprodce bug in Angular 9 when building with '--localize'

[GitHub Issue](https://github.com/angular/angular/issues/35420)

### Bug
Build exists with error message `Cannot read property 'startTag' of null` and aborts. Fails to create index.html.

## To reproduce
```bash
ng build --localize
```
## Cause
In index.html the link-tag is placed outside the html-tag. If the link-tag is moved to the correct place, the error goes away.

## Version info

```
Angular CLI: 9.0.2
Node: 12.10.0
OS: linux x64

Angular: 9.0.1
... animations, common, compiler, compiler-cli, core, forms
... language-service, localize, platform-browser
... platform-browser-dynamic, router
Ivy Workspace: Yes

Package                           Version
-----------------------------------------------------------
@angular-devkit/architect         0.900.2
@angular-devkit/build-angular     0.900.2
@angular-devkit/build-optimizer   0.900.2
@angular-devkit/build-webpack     0.900.2
@angular-devkit/core              9.0.2
@angular-devkit/schematics        9.0.2
@angular/cli                      9.0.2
@ngtools/webpack                  9.0.2
@schematics/angular               9.0.2
@schematics/update                0.900.2
rxjs                              6.5.4
typescript                        3.7.5
webpack                           4.41.2
```
