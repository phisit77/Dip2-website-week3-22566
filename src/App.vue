<script>
const fname = "";
const lname = "";
const userObject = { user: "mark", pass: "1234" };
const userArr = ["Elon", "Musk"];
const link = "https://www.google.com";
export default {
  data() {
    return { fname, lname, userObject, userArr, link };
  },
  methods: {
    thisArrowFunc: () => {
      const username2 = "bill";
      return username2 + " " + fname;
    },

    greeting: (age) => {
      return "Hello " + fname + " " + fname + age;
    },
  },
  computed: {
    fulName() {
      return this.fname + "" + this.lname;
    },
  },
};
</script>

<template>
  <div>
    <p>Full Name: {{ fulName }}</p>
    <p>
      <label for="">First Name: </label>
      <input type="text" v-model="fname" />
    </p>
    <p>
      <label for="">Last Name:</label>
      <input type="text" v-model="lname" />
    </p>
    <hr />

    <p>{{ thisArrowFunc() }}</p>
    <p>{{ greeting(50) }}</p>
    <a :href="link">Google</a>
    <h1>{{ fname }} {{ lname }}</h1>
    <h3>User:{{ userObject.user }}</h3>
    <h3>Pass:{{ userObject.pass }}</h3>
    <h3>{{ userArr[0] }} {{ userArr[1] }}</h3>
  </div>
</template>

<style></style>
