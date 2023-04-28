<script setup>
  import { mdiBatteryCharging, mdiNetworkStrength3 } from "@mdi/js";
  import moment from "moment";
  import { ref } from "vue";

  let currentTime = ref();

  setInterval(function () {
    currentTime.value = moment().format("h:mm:ss a");
  }, 1000);
</script>
<template>
  <v-system-bar>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="4">
          <div class="d-flex">
            {{ currentTime }}
            <v-spacer></v-spacer>
          </div>
        </v-col>
        <v-col cols="12" md="4">
          <v-spacer></v-spacer>
          <v-icon :icon="mdiNetworkStrength3"></v-icon>
          <v-icon :icon="mdiBatteryCharging"></v-icon>
        </v-col>
      </v-row>
    </v-container>
  </v-system-bar>
</template>
