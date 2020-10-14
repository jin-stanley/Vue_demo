<template>
  <v-app>
    <div class="v-app">
      <AppNavigationDrawer
        v-if="loggin"
        :handleLogout="handleLogout"
        :miniVariant="miniVariant"
      />
      <v-main>
        <AppBar
          :loggin="loggin"
          :handleLogin="handleLogin"
          :toggleMiniVariant="toggleMiniVariant"
        />
        <AppBoard />
      </v-main>
    </div>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {
    AppNavigationDrawer: () =>
      import("./components/Common/AppNavigationDrawer"),
    AppBoard: () => import("./components/Common/AppBoard"),
    AppBar: () => import("./components/Common/AppBar"),
  },
  methods: {
    toggleMiniVariant() {
      this.miniVariant = !this.miniVariant;
    },
    handleLogin() {
      this.loggin = true;
    },
    handleLogout() {
      this.loggin = false;
    },
  },
  data: () => ({
    miniVariant: false,
    loggin: false,
  }),
};
</script>

<style scoped>
.v-app {
  display: flex;
  flex-direction: row;
  height: 100%;
}
</style>