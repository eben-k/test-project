<template>
  <v-app>
    <div id="app">
      <router-view />
    </div>
  </v-app>
</template>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: "Lato";
  background: #e5e5e5;
  width: 120rem;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}
</style>
