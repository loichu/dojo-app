<template>
  <!-- Don't drop "q-app" class -->
  <div id="q-app">
    <q-layout>
      <div slot="header" class="toolbar">
        <button class="hide-on-drawer-visible" @click="$refs.drawer.open()">
          <i>menu</i>
        </button>
        <q-toolbar-title>
          EPFL Dojo
        </q-toolbar-title>
        <img src="~statics/16x16.png" class="responsive" title="EPFL Dojo FTW ʅʕ•ᴥ•ʔʃ" />
      </div>
      <!-- Left side Drawer -->
      <q-drawer ref="drawer">
        <div class="list platform-delimiter">
          <q-drawer-link icon="home" to="/">Home</q-drawer-link>
          <q-drawer-link icon="change_history" to="/events">Events</q-drawer-link>
          <q-drawer-link icon="line_weight" to="/archives">Timeline</q-drawer-link>
          <q-drawer-link icon="link" to="/links">Links</q-drawer-link>
          <q-drawer-link icon="lightbulb_outline" to="/ideas">Ideas</q-drawer-link>
          <q-drawer-link icon="grade" to="/epfl-topics">EPFL-topics</q-drawer-link>
          <q-drawer-link icon="people" to="/about">About</q-drawer-link>
        </div>
        <div class="version">
          v1.0.6 / v{{$q.version}}
        </div>
      </q-drawer>

      <router-view class="layout-view"></router-view>

      <!-- <div slot="footer" class="footer">
        <small>Check out <a href="https://github.com/epfl-dojo">EPFL-Dojo</a> gh repo.</small>
      </div>
    </q-layout> -->
  </div>
</template>

<script>
  /*
 * Root component
 */
  export default {}
</script>

<style>
.version {
  display:flex;
  align-items:center;
  justify-content:center;
  font-size: small;
}
.toolbar-title {
  text-align: center;
  padding: 0;
}
</style>
