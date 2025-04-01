<script>
  export default{
    data(){
      return {
        name: "Viresh Shah",
        status: "active",
        tasks : ["Task 1", "Task 2", "Task 3"],
        link: "https://www.google.com",
      };
    },
    methods : {
      toggleStatus(){
        if (this.status === "active"){
          this.status = "inactive";
        } else{
          this.status = "active";
        }
      },
    },
  }
</script>

<template>
  <!-- Vue directives -->
  <h1>{{ name }}</h1> 

  <!-- Else if directive in Vue -->
  <p v-if="status === 'active'">
    "User is active!"
  </p> 
  <p v-else-if="status === 'pending'">
    "Activation Pending"
  </p>
  <p v-else>
    "User is inactive!"
  </p>

  <!-- Looping directives -->
   <h3>Tasks:</h3>
   <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
   </ul>

   <!-- Bind directives -->
   <!-- <a v-bind:href="link" target="_blank">Click to open google.com</a> -->
   <a :href="link" target="_blank">Click to open google.com</a><br/>

   <!-- Events and Methods -->
    <button @click="toggleStatus">Change Status!</button>
  </template>

