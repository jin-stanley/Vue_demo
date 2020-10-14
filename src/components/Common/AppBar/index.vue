<template>
  <v-app-bar dark>
    <v-app-bar-nav-icon
      v-if="loggin"
      @click="toggleMiniVariant"
    ></v-app-bar-nav-icon>
    <v-toolbar-title>MathKit</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn @click="handleLogin" v-if="!loggin"> Login </v-btn>
    <div v-else>Hi, Stanley Jin</div>
  </v-app-bar>
</template>

<script>
export default {
  name: "AppBar",
  props: {
    loggin: Boolean,
    toggleMiniVariant: Function,
    handleLogin: Function,
  },
};
</script>

<style>
</style>