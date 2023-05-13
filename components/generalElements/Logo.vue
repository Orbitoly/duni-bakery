<script setup>
const runtimeConfig = useRuntimeConfig();
const logoUrl = runtimeConfig?.public?.LOGO || null;
</script>

<template>
  <NuxtLink to="/">
    <img v-if="logoUrl" :src="logoUrl" alt="Logo" class="object-contain h-10" />
    <div v-else class="flex font-bold text-lg gap-2 items-center">
      <img src="images/duni.jpeg" alt="Logo" class="object-contain h-12" />
      
      <span>Duni</span>
    </div>
  </NuxtLink>
</template>
