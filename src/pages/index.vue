<template>
  <v-menu v-if="open" :close-on-content-click="false">
    <template #activator="{ props }">
      <v-btn v-bind="props">Open</v-btn>
    </template>
    <v-sheet class="pa-4">
      <div class="d-flex">
        <v-menu>
          <template #activator="{ props }">
            <v-btn style="display: block" v-bind="props">Sub menu</v-btn>
          </template>
          <v-sheet class="pa-4"> Click back in the input</v-sheet>
        </v-menu>
        <v-text-field style="width: 400px"></v-text-field>
      </div>
    </v-sheet>
  </v-menu>

  <router-link to="other-route" style="margin-left: 48px"> leave </router-link>
</template>

<script setup>
import { ref } from "vue";

const open = ref(true);
</script>
