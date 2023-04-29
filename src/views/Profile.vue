<script setup>
  import { mdiAccountOutline, mdiCameraOutline, mdiChevronRight, mdiCogOutline, mdiHelpCircleOutline, mdiInformationOutline, mdiKeyVariant, mdiLightningBolt, mdiLogoutVariant } from "@mdi/js";
  import { reactive } from "vue";

  const profile = reactive([
    {
      subtitle: "Settings",
      item: [
        {
          icon: mdiCogOutline,
          title: "App Settings",
          href: "/",
        },
      ],
    },
    {
      subtitle: "Account",
      item: [
        {
          icon: mdiAccountOutline,
          title: "Change Account Name",
          href: "/",
        },
        {
          icon: mdiKeyVariant,
          title: "Change Account Password",
          href: "/",
        },
        {
          icon: mdiCameraOutline,
          title: "Change Account Image",
          href: "/",
        },
      ],
    },
    {
      subtitle: "To Do",
      item: [
        {
          icon: mdiInformationOutline,
          title: "About Us",
          href: "/",
        },
        {
          icon: mdiHelpCircleOutline,
          title: "FAQ",
          href: "/",
        },
        {
          icon: mdiCogOutline,
          title: "Help & Feedback",
          href: "/",
        },
        {
          icon: mdiLightningBolt,
          title: "Support",
          href: "/",
        },
        {
          icon: mdiLogoutVariant,
          title: "Log Out",
          href: "/",
        },
      ],
    },
  ]);
</script>
<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12" md="4">
        <v-card flat color="transparent">
          <v-card-text class="text-center">
            <v-avatar size="120">
              <v-img cover src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"></v-img>
            </v-avatar>
          </v-card-text>
          <v-card-title class="text-center pb-0">Luis Diaz</v-card-title>
          <v-card-text class="text-center">10 tasks left | 20 tasks done</v-card-text>
        </v-card>
        <template v-for="item in profile">
          <v-list-subheader v-text="item['subtitle']"></v-list-subheader>
          <v-card flat border>
            <template v-for="(sub, i) in item.item">
              <v-list-item :to="sub['href']" class="py-4" :class="sub['title'] == 'Log Out' ? 'text-red' : ''">
                <template #prepend>
                  <v-icon :icon="sub['icon']"></v-icon>
                </template>
                <v-list-item-title v-text="sub['title']"></v-list-item-title>
                <template #append v-if="sub['title'] !== 'Log Out'">
                  <v-icon :icon="mdiChevronRight"></v-icon>
                </template>
              </v-list-item>
              <v-divider v-if="item.length !== i + 1"></v-divider>
            </template>
          </v-card>
        </template>
      </v-col>
    </v-row>
  </v-container>
</template>
