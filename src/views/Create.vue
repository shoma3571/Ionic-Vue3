<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Create Task</ion-title>
        <ion-icon :icon="arrowBack" @click="() => router.back()"></ion-icon>
      </ion-toolbar>
    </ion-header>
    
    <ion-content id="create" :fullscreen="true">
      <ion-list>
          <ion-item>
              <ion-input placeholder="title"></ion-input>
          </ion-item>
          <ion-item>
              <ion-textarea placeholder="memo"></ion-textarea>
          </ion-item>
          <ion-item>
              <ion-label>Ends</ion-label>
              <ion-datetime value="2012-12-15" placeholder="Select Date"></ion-datetime>
          </ion-item>
      </ion-list>
      <ion-button id="create-btn">Create</ion-button>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonDatetime, IonList, IonItem, IonInput, IonTextarea, IonButton, IonLabel, IonIcon } from '@ionic/vue';
import { defineComponent } from 'vue';

import { arrowBack } from 'ionicons/icons';
import { useRouter } from 'vue-router';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonDatetime,
    IonList,
    IonItem,
    IonInput,
    IonTextarea,
    IonButton,
    IonLabel,
    IonIcon
  },
  setup(){
    return{
      router: useRouter(),
      arrowBack
    }
  }
});
</script>

<style scoped>
#create{
    text-align: center;
}

#create-btn{
    margin-top: 30px;
}
</style>