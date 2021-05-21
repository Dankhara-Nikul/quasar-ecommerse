<template>
  <q-layout view="lHh Lpr fff">

    <q-header reveal elevated class="bg-grey-3 text-dark" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          
          <img src="~assets/logo.png" width="128">
        </q-toolbar-title>
        <q-btn flat round dense icon="search" />
        <q-btn dense flat round icon="menu" @click="right = !right" />
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="Page One" />
        <q-route-tab to="/page2" label="Page Two" />
        <q-route-tab to="/page3" label="Page Three" />
      </q-tabs>
    </q-header>

    <q-drawer v-model="right" side="right" overlay behavior="mobile" bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal elevated class="bg-dark text-white">
      <q-toolbar>
        <q-toolbar-title>
            <img src="~assets/logo.png" width="128">
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      right: false
    }
  }
}
</script>