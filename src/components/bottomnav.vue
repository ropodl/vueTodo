<script setup>
  import { mdiAccountOutline, mdiCalendarMonthOutline, mdiClockTimeEightOutline, mdiHome, mdiPlus } from "@mdi/js";
</script>
<template>
  <v-bottom-navigation>
          <v-btn to="/">
            <v-icon :icon="mdiHome"></v-icon>
            <span>Home</span>
          </v-btn>
          <v-btn to="/calendar">
            <v-icon :icon="mdiCalendarMonthOutline"></v-icon>
            <span>Calendar</span>
          </v-btn>
          <v-btn variant="flat" class="bump-icon">
            <v-icon :icon="mdiPlus"></v-icon>
            <span>New Task</span>
          </v-btn>
          <v-btn to="/focus">
            <v-icon :icon="mdiClockTimeEightOutline"></v-icon>
            <span>Focus</span>
          </v-btn>
          <v-btn to="/profile">
            <v-icon :icon="mdiAccountOutline"></v-icon>
            <span>Profile</span>
          </v-btn>
  </v-bottom-navigation>
</template>
