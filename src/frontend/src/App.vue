<template>
  <div>
    <MainMenu/>
    <router-view/>
  </div>
</template>

<script>
import MainMenu from "./components/MainMenu.vue";
export default {
    name: 'App',
    components: {
        MainMenu
    },
    created() {
        this.$store.dispatch('getArticles')
    },
}

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
}
</style>
