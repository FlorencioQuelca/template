<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> tesis </q-toolbar-title>

        <div>fqm</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> enlaces </q-item-label>

        <q-item clickable to="/" exact active-class="my-menu-link">
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>
          <q-item-section>Principal</q-item-section>
        </q-item>
        <q-item clickable to="documentos" exact active-class="my-menu-link">
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>
          <q-item-section>documentos</q-item-section>
        </q-item>
        <q-item clickable to="sobre_mi" exact active-class="my-menu-link">
          <q-item-section avatar>
            <q-icon name="inbox" />
          </q-item-section>
          <q-item-section>Sobre Mi</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>

<style lang="sass">
.my-menu-link
  color: white
  background: #F2C037
</style>
