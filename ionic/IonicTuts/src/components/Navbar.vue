<template>
    <ion-header>
      <ion-toolbar color="light">
        <ion-title class="title">Viresh's Portfolio</ion-title>
  
        <ion-buttons slot="end" class="nav-links">
          <ion-button fill="clear" @click="navigateTo('/')">Home</ion-button>
          <ion-button fill="clear" @click="navigateTo('/projects')">Projects</ion-button>
          <ion-button fill="clear" @click="navigateTo('/about')">About</ion-button>
          <ion-button fill="clear" @click="navigateTo('/contact')">Contact</ion-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>
  </template>
  
  <script setup>
  import { IonHeader, IonToolbar, IonTitle, IonButtons, IonButton } from '@ionic/vue'
  import { useRouter } from 'vue-router'
  
  const router = useRouter()
  
  const navigateTo = (path) => {
    router.push(path)
  }
  </script>
  
  <style scoped>
  .title {
    font-weight: bold;
    font-size: 1.3rem;
    padding-left: 1rem;
  }
  
  .nav-links ion-button {
    font-size: 1rem;
    margin: 0 0.3rem;
    color: #333;
  }
  </style>
  