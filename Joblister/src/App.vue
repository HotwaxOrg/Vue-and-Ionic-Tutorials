<script setup>
  import Navbar from '@/components/Navbar.vue';
  import Hero from '@/components/Hero.vue';
  import HomeCard from '@/components/HomeCards.vue';
  import Joblisting from '@/components/Joblisting.vue';
</script>
<template>
  <Navbar />
  <Hero title="Test Props" subtitle="Test Prop Subtitel"/>
  <HomeCard />
  <Joblisting :limit="3" :showButton="true"/>
</template>

