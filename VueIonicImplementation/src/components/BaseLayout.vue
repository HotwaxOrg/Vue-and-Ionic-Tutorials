<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>{{ pageTitle }}</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content>
           <slot />
        </ion-content>
    </ion-page>
</template>

<script setup lang="ts">
    import { IonPage, IonHeader, IonTitle, IonContent, IonToolbar } from '@ionic/vue';
    import { defineProps } from 'vue';

    const props = defineProps(["pageTitle"])
</script>