<template>
  <h1>HELLO {{ formValues.name }}</h1>
  <h3>Country = {{ formValues.country }}</h3>
  <h4>Remote Work = {{ formValues.remoteWork }}</h4>

  <form @submit="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>

    <div>
      <label for="country">Country</label>
      <select multiple id="country" v-model="formValues.country">
        <option value="">Select a Value</option>
        <option value="india">India</option>
        <option value="srilanka">Sri Lanka</option>
      </select>
    </div>

    <div>
      <label for="remoteWork">WFH Available for 0530 GMT</label>
      <input type="checkbox" id="remoteWork" v-model="formValues.name" />
    </div>

    <div>
      <label for="age">Age</label>
      <input type="text" id="age" v-model.number="formValues.age" />
    </div>

    <div>
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      formValues: {
        name: "Pandu",
        country: [],
        remoteWork: false,
        age: null,
      },
    };
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log(event);
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
