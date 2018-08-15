<template>
  <div id="app">
    <v-app dark class="black">
      <v-content>
        <v-container fluid fill-height class="ma-0 pa-0">
            <router-view></router-view>
        </v-container>
      </v-content>
    </v-app>
  </div>
</template>

<script>
  export default {
    name: 'screens'
  }
</script>
