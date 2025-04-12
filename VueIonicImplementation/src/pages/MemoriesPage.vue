<template>
    <base-layout pageTitle="All Memories">
        <ion-list>
            <ion-item router-link="/memories/1">A trip into the mountains</ion-item>
            <ion-item>Surfing the sea</ion-item>
            <ion-item>Good eating</ion-item>
        </ion-list>
    </base-layout>
</template>

<script setup lang="ts">
    import { IonList, IonItem } from '@ionic/vue';
</script>