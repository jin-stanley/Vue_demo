<template>
  <v-navigation-drawer :mini-variant="miniVariant" mini-variant-width="58" dark>
    <v-list>
      <v-list-item>
        <v-list-item-content v-if="!miniVariant">
          <!-- &&& Here will catch username and email -->
          <v-list-item-title class="title"> Stanley Jin </v-list-item-title>
          <v-list-item-subtitle>jinwangjitai@gmail.com</v-list-item-subtitle>
        </v-list-item-content>
        <v-avatar v-if="miniVariant">
          <!-- &&& Here will catch user avatar -->
          <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
        </v-avatar>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list>
      <v-list-item to="/">
        <v-list-item-icon>
          <v-icon>mdi-monitor</v-icon>
        </v-list-item-icon>
        <v-list-item-title>Dashboard</v-list-item-title>
      </v-list-item>
      <v-list-item to="/about">
        <v-list-item-icon>
          <v-icon>mdi-information</v-icon>
        </v-list-item-icon>
        <v-list-item-title>About</v-list-item-title>
      </v-list-item>
      <v-list-item to="/sandbox">
        <v-list-item-icon>
          <v-icon>mdi-toolbox</v-icon>
        </v-list-item-icon>
        <v-list-item-title>SandBox</v-list-item-title>
      </v-list-item>
    </v-list>

    <v-spacer></v-spacer>

    <template v-slot:append>
      <v-divider></v-divider>
      <v-list>
        <v-list-item @click="handleLogout">
          <v-list-item-icon>
            <v-icon>mdi-login-variant</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Logout</v-list-item-title>
        </v-list-item>
      </v-list>
    </template>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "AppNavigationDrawer",
  props: {
    miniVariant: Boolean,
    handleLogout: Function,
  },
};
</script>

<style>
</style>