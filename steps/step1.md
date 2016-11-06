[__prod__]: #
[{]: <region> (header)

[}]: #
[{]: <region> (body)
# Create Tortilla Tab

Create Tortilla view:

[{]: <helper> (diff_step 1.1)
#### Step 1.1: Create tortilla view

##### Added src/pages/tortilla/tortilla.html
```diff
@@ -0,0 +1,11 @@
+┊  ┊ 1┊<ion-header>
+┊  ┊ 2┊  <ion-navbar>
+┊  ┊ 3┊    <ion-title>
+┊  ┊ 4┊      Tortilla
+┊  ┊ 5┊    </ion-title>
+┊  ┊ 6┊  </ion-navbar>
+┊  ┊ 7┊</ion-header>
+┊  ┊ 8┊
+┊  ┊ 9┊<ion-content padding>
+┊  ┊10┊
+┊  ┊11┊</ion-content>
```
[}]: #

Create Tortilla component:

[{]: <helper> (diff_step 1.2)
#### Step 1.2: Create tortilla component

##### Added src/pages/tortilla/tortilla.ts
```diff
@@ -0,0 +1,15 @@
+┊  ┊ 1┊import { Component } from '@angular/core';
+┊  ┊ 2┊
+┊  ┊ 3┊import { NavController } from 'ionic-angular';
+┊  ┊ 4┊
+┊  ┊ 5┊@Component({
+┊  ┊ 6┊  selector: 'page-tortilla',
+┊  ┊ 7┊  templateUrl: 'tortilla.html'
+┊  ┊ 8┊})
+┊  ┊ 9┊export class TortillaPage {
+┊  ┊10┊
+┊  ┊11┊  constructor(public navCtrl: NavController) {
+┊  ┊12┊
+┊  ┊13┊  }
+┊  ┊14┊
+┊  ┊15┊}
```
[}]: #

Import Tortilla component:

[{]: <helper> (diff_step 1.3)
#### Step 1.3: Import tortilla component

##### Changed src/app/app.module.ts
```diff
@@ -4,6 +4,7 @@
 ┊ 4┊ 4┊import { AboutPage } from '../pages/about/about';
 ┊ 5┊ 5┊import { ContactPage } from '../pages/contact/contact';
 ┊ 6┊ 6┊import { HomePage } from '../pages/home/home';
+┊  ┊ 7┊import { TortillaPage } from '../pages/tortilla/tortilla';
 ┊ 7┊ 8┊import { TabsPage } from '../pages/tabs/tabs';
 ┊ 8┊ 9┊
 ┊ 9┊10┊@NgModule({
```
```diff
@@ -12,6 +13,7 @@
 ┊12┊13┊    AboutPage,
 ┊13┊14┊    ContactPage,
 ┊14┊15┊    HomePage,
+┊  ┊16┊    TortillaPage,
 ┊15┊17┊    TabsPage
 ┊16┊18┊  ],
 ┊17┊19┊  imports: [
```
```diff
@@ -23,6 +25,7 @@
 ┊23┊25┊    AboutPage,
 ┊24┊26┊    ContactPage,
 ┊25┊27┊    HomePage,
+┊  ┊28┊    TortillaPage,
 ┊26┊29┊    TabsPage
 ┊27┊30┊  ],
 ┊28┊31┊  providers: []
```
[}]: #

Add Tortilla tab to tabs view:

[{]: <helper> (diff_step 1.4)
#### Step 1.4: Add tortila tab to tabs view

##### Changed src/pages/tabs/tabs.html
```diff
@@ -2,4 +2,5 @@
 ┊2┊2┊  <ion-tab [root]="tab1Root" tabTitle="Home" tabIcon="home"></ion-tab>
 ┊3┊3┊  <ion-tab [root]="tab2Root" tabTitle="About" tabIcon="information-circle"></ion-tab>
 ┊4┊4┊  <ion-tab [root]="tab3Root" tabTitle="Contact" tabIcon="contacts"></ion-tab>
+┊ ┊5┊  <ion-tab [root]="tab4Root" tabTitle="Tortilla" tabIcon="pizza"></ion-tab>
 ┊5┊6┊</ion-tabs>
```
[}]: #

Define Tortilla root in tabs component:

[{]: <helper> (diff_step 1.5)
#### Step 1.5: Define tortilla root in tabs component

##### Changed src/pages/tabs/tabs.ts
```diff
@@ -3,6 +3,7 @@
 ┊3┊3┊import { HomePage } from '../home/home';
 ┊4┊4┊import { AboutPage } from '../about/about';
 ┊5┊5┊import { ContactPage } from '../contact/contact';
+┊ ┊6┊import { TortillaPage } from '../tortilla/tortilla';
 ┊6┊7┊
 ┊7┊8┊@Component({
 ┊8┊9┊  templateUrl: 'tabs.html'
```
```diff
@@ -13,6 +14,7 @@
 ┊13┊14┊  tab1Root: any = HomePage;
 ┊14┊15┊  tab2Root: any = AboutPage;
 ┊15┊16┊  tab3Root: any = ContactPage;
+┊  ┊17┊  tab4Root: any = TortillaPage;
 ┊16┊18┊
 ┊17┊19┊  constructor() {
```
[}]: #
[}]: #
[{]: <region> (footer)
[{]: <helper> (nav_step)

[}]: #
[}]: #