<script setup>
  import { RouterLink, useRoute } from 'vue-router';

  const logo = 'public/images/logo.png';

  const isActiveLink = (routePath) => {
    const route = useRoute();
    return route.path === routePath;
  };
</script>

<template>
    <nav class="bg-green-700 border-b border-green-500">
      <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
        <div class="flex h-20 items-center justify-between">
          <div
            class="flex flex-1 items-center justify-center md:items-stretch md:justify-start"
          >
            <!-- Logo -->
            <RouterLink class="flex flex-shrink-0 items-center mr-4" to="/">
              <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
              <span class="hidden md:block text-white text-2xl font-bold ml-2"
                >Vue Jobs</span
              >
            </RouterLink>
            <div class="md:ml-auto">
              <div class="flex space-x-2">
                <RouterLink
                  to="/"
                  :class="['text-white', 'px-3', 'py-2', 'rounded-md', isActiveLink('/') ? 'bg-green-900' : 'hover:bg-gray-900 hover:text-white']"
                  >Home
                </RouterLink>
                <RouterLink
                  to="/jobs"
                  :class="['text-white', 'px-3', 'py-2', 'rounded-md', isActiveLink('/jobs') ? 'bg-green-900' : 'hover:bg-gray-900 hover:text-white']"
                  >Jobs</RouterLink
                >
                <RouterLink
                  to="/add-job"
                  :class="['text-white', 'px-3', 'py-2', 'rounded-md', isActiveLink('/add-job') ? 'bg-green-900' : 'hover:bg-gray-900 hover:text-white']"
                  >Add Job</RouterLink
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </nav>
</template>