

<template>
  <NuxtLoadingIndicator />
    <NuxtLayout>
      <keep-alive>
        <AuthenticationManager/>
      </keep-alive>
      <NuxtPage/>
    </NuxtLayout>
</template>

<script setup lang="ts">

import {KliveAPIUrl} from '~/scripts/APIInterface'
import Navbar from './layouts/navbar.vue';
</script>

<style>
.page-enter-active,
.page-leave-active {
  transition: all 0.4s;
}

.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(1rem);
}

.layout-enter-active,
.layout-leave-active {
  transition: all 0.4s;
}
.layout-enter-from,
.layout-leave-to {
  filter: grayscale(1);
  opacity: 0;
  filter: blur(1rem);
}
</style>