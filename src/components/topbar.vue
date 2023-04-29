<script setup>
  import { mdiBatteryCharging, mdiNetworkStrength3, mdiWifi } from "@mdi/js";
  import moment from "moment";
  import { ref } from "vue";

  let currentTime = ref();

  setInterval(function () {
    currentTime.value = moment().format("h:mm:ss a");
  }, 1000);
</script>
<template>
  <v-system-bar>
    <v-container fluid>
      <v-row justify="center">
        <v-col cols="12" md="4">
          <div class="d-flex text-uppercase">
            {{ currentTime }}
            <v-spacer></v-spacer>
            <v-icon :icon="mdiWifi"></v-icon>
            <v-icon :icon="mdiNetworkStrength3"></v-icon>
            <v-icon :icon="mdiBatteryCharging"></v-icon>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-system-bar>
</template>
