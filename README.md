<p align="center">
  <h1 align="center">AngularFire2</h1>
  <p align="center">The official library for Firebase and Angular 2</p>
</p>

### AngularFire2 is currently not on new Firebase 3.0 SDK, but there is an update in progress.

[![Build Status](https://travis-ci.org/angular/angularfire2.svg?branch=master)](https://travis-ci.org/angular/angularfire2) [![Join the chat at https://gitter.im/angular/angularfire2](https://badges.gitter.im/angular/angularfire2.svg)](https://gitter.im/angular/angularfire2?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Status: Beta

## What is AngularFire2?

- **Observable based** - Use the power of rxjs, Angular 2, and Firebase.
- **Realtime bindings** - Synchronize collections as objects or lists.
- **Authentication** - Monitor authentication state in realtime.

## Install

```bash
npm install angularfire2 firebase --save
```

## Example use:

```ts
import {Component} from '@angular/core';
import {AngularFire, FirebaseListObservable} from 'angularfire2';

@Component({
  selector: 'project-name-app',
  template: `
  <ul>
    <li *ngFor="let item of items | async">
      {{ item.name }}
    </li>
  </ul>
  `
})
export class MyApp {
  items: FirebaseListObservable<any[]>;
  constructor(af: AngularFire) {
    this.items = af.database.list('/items');
  }
}
```

## Developer Guide
If you want to get started quickly on building with AngularFire2, check out our
5 step developer guide that will teach you everything you need to know to be 
dangerous with AngularFire2.

1. [Installation & Setup](docs/1-install-and-setup.md)
2. [Retreiving data as objects - FirebaseObjectObservable](docs/2-retrieving-data-as-objects.md)
3. [Retreiving data as lists - FirebaseListObservable](docs/3-retrieving-data-as-lists.md)
4. [Querying lists](docs/4-querying-lists.md)
5. [User Authentication - FirebaseAuthentication](docs/5-user-authentication.md)

## [API Reference](docs/api-reference.md)
