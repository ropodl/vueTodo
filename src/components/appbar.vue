<script setup>
  import { useRoute } from "vue-router";
  const route = useRoute();
  console.log(route);
</script>
<template>
  <v-app-bar>
    <v-container class="pa-0">
      <v-row justify="center">
        <div class="text-capitalize font-weight-bold">
          {{ route["name"] }}
        </div>
      </v-row>
    </v-container>
  </v-app-bar>
</template>
