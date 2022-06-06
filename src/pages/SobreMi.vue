<template>
  <q-page class="flex flex-center">
    <h1>{{ hora }}</h1>
    <h1>{{ horaes }}</h1>
  </q-page>
</template>

<script setup>
import { computed, ref } from "vue";
import moment from "moment";
moment.locale("es");
const letra = ref("hola123");
const hora = ref(moment().format("MMMM D YYYY, h:mm:ss a"));

const horaes = computed(() => moment().format("MMMM D YYYY, h:mm:ss a"));
</script>
