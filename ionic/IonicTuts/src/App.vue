<template>
  <ion-app>
    <ion-router-outlet />
    <Navbar/>
    <CardComp />
    <ion-checkbox>
      Check Me!
    </ion-checkbox>
    <ion-chip>
    <ion-avatar>
      <img alt="Silhouette of a person's head" src="https://ionicframework.com/docs/img/demos/avatar.svg" />
    </ion-avatar>
    <ion-label>Avatar Chip</ion-label>
    <ion-icon :icon="closeCircle"></ion-icon>
  </ion-chip>

  <ion-chip>
    <ion-icon :icon="pin" color="primary"></ion-icon>
    <ion-label>Icon Chip</ion-label>
    <ion-icon :icon="close"></ion-icon>
  </ion-chip>
  </ion-app>
</template>

<script setup lang="ts">
import { IonApp, IonRouterOutlet } from '@ionic/vue';
import { IonCheckbox } from '@ionic/vue';
import { IonChip, IonAvatar, IonLabel, IonIcon } from '@ionic/vue';
import Navbar from '@/components/Navbar.vue';
import CardComp from '@/components/Cards.vue';
</script>
