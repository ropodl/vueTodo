<script setup>
  import { defineAsyncComponent, ref } from "vue";
  import { RouterView } from "vue-router";
  const topbar = defineAsyncComponent(() => import("@/components/topbar"));
  const appbar = defineAsyncComponent(() => import("@/components/appbar"));
  const bottomnav = defineAsyncComponent(() => import("@/components/bottomnav"));

  let value = ref(1);
</script>
<template>
  <v-app>
    <topbar />
    <appbar />
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
