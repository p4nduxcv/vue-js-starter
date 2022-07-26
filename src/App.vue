<template>
  <h1>HELLO {{ name }}</h1>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
  <div v-bind:id="headingId">Heading</div>
  <button v-bind:id="headingId">Button</button>
  <h1 v-if="num == 0">Number Is ZERO</h1>
  <h1 v-if="num > 0">Number Is POssitive</h1>
  <h1 v-if="num < 0">Number Is Negative</h1>
  <h1 v-else>Number Is Not ZERO</h1>

  <h2 v-show="isShow">RA</h2>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      name: "PANDULA DAN",
      channel: "<b>Mastach</b>",
      hack: `<a href='#' onclick="alert('You Have Been HAcked')">CLIKC<a/>`,
      headingId: "heading",
      isDisabled: true,
      num: 4,
      isShow: true,
    };
  },
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
