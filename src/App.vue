<template>
  <h1>Volume Tracker - {{ volume }}</h1>
  <button @click="volume += 2">+</button>
  <button @click="volume -= 2">-</button>

  <input type="text" v-model="movie" />
  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      volume: 0,
      movie: "GIO",
      movieInfo: {
        title: "A",
        actor: "E",
      },
    };
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log(event);
    },
  },
  computed: {
    tot() {
      return this.cars.reduce((acc, curr) => (acc = acc + curr.price), 0);
    },
  },
  watch: {
    volume(newVal, oldVal) {
      if (newVal > oldVal && newVal === 16) {
        alert("Kana Palei Whotto!");
      }
    },
    movie: {
      handler(newVal) {
        console.log(`Calling API with movie Name = ${newVal}`);
      },
      immediate: true,
    },
    movieInfo: {
      handler(newVal) {
        console.log(`Calling API with movie Info = ${newVal.title} and`);
      },
      deep: true,
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: olivedrab;
}
.sold-out {
  color: red;
}
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
