<template>
  <div id="app">
    <input type="button" value="-" @click="minus" />
    {{ count }}
    <input type="button" value="+" @click="plus" />
  </div>
</template>

<script>
export default {
  name: "App",
  computed: {
    count() {
      return this.$store.state.count
    }
  },
  methods: {
    minus() {
      this.$store.commit('minus')
    },
    plus() {
      this.$store.commit('plus')
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
