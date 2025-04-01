<script>
  export default{
    data(){
      return {
        name: "Viresh Shah",
        status: "active",
      };
    },
  }
</script>

<template>
  <h1>{{ name }}</h1> 
  <p v-if="status === 'active'">
    "User is active!"
  </p> 
  <p v-else-if="status === 'pending'">
    "Activation Pending"
  </p>
  <p v-else>
    "User is inactive!"
  </p>
</template>

