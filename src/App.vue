<template>
  <!-- <h1>HELLO {{ name }}</h1>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
  <div v-bind:id="headingId">Heading</div>
  <button v-bind:id="headingId">Button</button>
  <h1 v-if="num == 0">Number Is ZERO</h1>
  <h1 v-if="num > 0">Number Is POssitive</h1>
  <h1 v-if="num < 0">Number Is Negative</h1>
  <h1 v-else>Number Is Not ZERO</h1>

  <h2 v-show="isShow">RA</h2> -->
  <!-- <div v-show="isShow">
    <ul v-for="name in namesArr" :key="name">
      <li>{{ name }}</li>
    </ul>
  </div>

  <div v-for="actor in actors" :key="actor.name" v-show="true">
    <h2>{{ actor.name }}</h2>
    <h4 v-for="movie in actor.movies" :key="movie">{{ movie }}</h4>
  </div> -->

  <h2>Add Method = {{ add(2, 3, 4) }}</h2>
  <h3>Add Method = {{ multi(4) }}</h3>

  <h1>{{ name }}</h1>
  <div><button v-on:click="changeName">Change name</button></div>

  <h1>{{ count }}</h1>
  <div><button v-on:click="incre">Increment Count</button></div>
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
      isShow: false,
      namesArr: ["Pa", "ND", "UL", "A"],
      actors: [
        { name: "Nimal", movies: ["XXX, ZZZ, YYY"] },
        { name: "Nimal-Pa", movies: ["XEX, ZEZ, YEY"] },
      ],
      baseMultiplier: 5,
      count: 1,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multi(num) {
      return num * this.baseMultiplier;
    },
    incre() {
      return this.count++;
    },
    changeName(event) {
      console.log(event);
      return (this.name = "Kyle");
    },
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
