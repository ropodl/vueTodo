<script setup>
  import { defineAsyncComponent, ref } from "vue";
  import { useRoute } from "vue-router";

  const route = useRoute();

  const topbar = defineAsyncComponent(() => import("@/components/topbar"));
  const appbar = defineAsyncComponent(() => import("@/components/appbar"));
  const bottomnav = defineAsyncComponent(() => import("@/components/bottomnav"));

  let value = ref(1);
</script>
<template>
  <v-app>
    <topbar />
    <appbar v-if="route.name !== 'profile'" />
    <v-main>
      <RouterView />
    </v-main>
    <bottomnav />
  </v-app>
</template>
<style>
  .bump-icon {
    background-color: rgb(var(--v-theme-primary)) !important;
  }
</style>
