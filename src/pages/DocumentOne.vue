<template>
  <q-page class="flex flex-center">
    <h1>{{ letra }}a</h1>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "DocumentOne",
  setup() {
    return {
      letra: ref("comesdasdasr"),
    };
  },
});
</script>
