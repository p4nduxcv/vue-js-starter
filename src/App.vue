<template>
  <h1>
    Total of All Cars =
    {{ tot }}
  </h1>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      cars: [
        { id: 1, model: "Toyota", price: 800 },
        { id: 2, model: "Suzuki", price: 9000 },
      ],
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
