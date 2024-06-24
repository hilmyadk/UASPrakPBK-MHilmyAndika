<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-cyan text-white">
      <q-toolbar class="justify-center">
        <q-toolbar-title class="header-title">
          Weather App
        </q-toolbar-title>
        <q-btn-dropdown flat icon="menu" class="text-white">
          <q-list>
            <q-item clickable tag="router-link" to="/">
              <q-item-section>
                <q-item-label>Home</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable tag="router-link" to="/tugas1">
              <q-item-section>
                <q-item-label>Tugas 1</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable tag="router-link" to="/tugas2">
              <q-item-section>
                <q-item-label>Tugas 2</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable tag="router-link" to="/tugas3">
              <q-item-section>
                <q-item-label>Tugas 3</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable tag="router-link" to="/tugas4">
              <q-item-section>
                <q-item-label>Tugas 4</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable tag="router-link" to="/tugas5">
              <q-item-section>
                <q-item-label>Tugas 5</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable tag="router-link" to="/tugas6">
              <q-item-section>
                <q-item-label>Tugas 6</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-btn-dropdown>
      </q-toolbar>
    </q-header>

    <q-page-container class="page-background">
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          &copy; 2024 Hilmyadk. All Rights Reserved.
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import Weather from './components/Weather.vue';

export default {
  name: 'App',
  components: {
    Weather,
  },
};
</script>

<style>
.header-title {
  font-size: 24px;
  color: black;
  text-align: center;
  font-weight: bold;
}

.page-background {
  background-image: url('src/assets/gambar.png');
  background-size: cover;
}
</style>
