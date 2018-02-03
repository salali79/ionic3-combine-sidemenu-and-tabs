# ionic3 combine sidemenu and tabs navigation




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