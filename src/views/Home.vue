<script setup>
  import { reactive } from "vue";

  const todos = reactive([
    {
      title: "This is a test",
      content: "Some description of the todo",
    },
    {
      title: "This is a test",
      content: "Some description of the todo",
    },
  ]);
</script>
<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12" md="4">
        <v-card border class="mb-3" v-for="todo in todos">
          <v-card-title>{{ todo.title }}</v-card-title>
          <v-card-text>{{ todo.content }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
