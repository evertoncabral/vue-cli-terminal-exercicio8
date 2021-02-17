<template>
  <div id="app">
    <h1 v-if="state === 'loading'">Loading API</h1>
    <h1 v-else-if="state === 'error'">Error na API</h1>
    <h1 v-else-if="messages.length === 0">Sem dados disponíveis na API</h1>
    <h1 v-else>{{ messages }}</h1>
    <br />
    <h1 v-show="true">DIRETIVAS v-show</h1>
    <a v-bind:href="url">Site do Google</a>
    <br>
    <a :href="url2">Site do Google</a>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      state: "loading",
      messages: [],
      show: true,
      url: "www.google.com.br",
       url2: "www.google.com.br",

    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
