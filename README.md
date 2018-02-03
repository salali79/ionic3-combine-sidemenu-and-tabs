# ionic3 combine sidemenu and tabs navigation

## Create Pages

```bash
C:\Users\wk647\Desktop\Tourplan> ionic g page itemone
C:\Users\wk647\Desktop\Tourplan> ionic g page itemtwo
C:\Users\wk647\Desktop\Tourplan> ionic g page itemthree
```

## **src/app/app.module.ts**

```typescript
...
import { ItemonePage } from '../pages/itemone/itemone';
import { ItemtwoPage } from '../pages/itemtwo/itemtwo';
import { ItemthreePage } from '../pages/itemthree/itemthree';

declarations: [
    MyApp,
    HomePage,
    ListPage,
    ItemonePage,
    ItemtwoPage,
    ItemthreePage
  ],
  ...
  entryComponents: [
    MyApp,
    HomePage,
    ListPage,
    ItemonePage,
    ItemtwoPage,
    ItemthreePage
  ],
...
```

### **page/home/home.ts**

```typescript
...
import { ItemonePage } from '../itemone/itemone';
import { ItemtwoPage } from '../itemtwo/itemtwo';
import { ItemthreePage } from '../itemthree/itemthree';

export class HomePage {
    tab1Root = ItemonePage;
    tab2Root = ItemtwoPage;
    tab3Root = ItemthreePage;
...
```


### **page/home/home.html**

```typescript
<ion-content>
...
  <ion-tabs>
    <ion-tab [root]="tab1Root" tabTitle="item one" tabIcon="home"></ion-tab>
    <ion-tab [root]="tab2Root" tabTitle="item two" tabIcon="information-circle"></ion-tab>
    <ion-tab [root]="tab3Root" tabTitle="item three" tabIcon="contacts"></ion-tab>
  </ion-tabs>
</ion-content>
```
<div width="100%">
<img src="https://raw.githubusercontent.com/wkddnjset/wkddnjset.github.io/master/_posts/images/2018-02-04/ionic_01.png" width="300" margin-right="100px"/>
<img src="https://raw.githubusercontent.com/wkddnjset/wkddnjset.github.io/master/_posts/images/2018-02-04/ionic_02.png" width="300"/>
 </div>
You can remove all header tags in TabsPage.html, It will look like left image
