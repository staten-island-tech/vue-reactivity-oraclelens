<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      checkedNames: [],
      selected: "",
    };
  },
  /*   component: {},
  data() {
    return {
      student: "help, i am so bad at algebra 2",
      graduated: true,
      animals: ["pig", "cow", "horse", "chicken"],
      loggedin: false,
      message: "",
    };
  },
  methods: {
    authState: function () {
      if (this.loggedin === false) {
        this.loggedin = true;
      } else {
        this.loggedin = false;
      }
    },
  }, */
};
</script>

<template>
  <input type="checkbox" id="jack" value="jack" v-model="checkedNames" />
  <label for="jack">Jack</label>
  <input type="checkbox" id="sally" value="sally" v-model="checkedNames" />
  <label for="sally">Sally</label>
  <input type="checkbox" id="yuh" value="yuh" v-model="checkedNames" />
  <label for="yuh">Yuh</label>

  <select v-model="selected">
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>

  <span>{{ selected }}</span>

  <br />
  <span>Checked names: {{ checkedNames }}</span>

  <main>
    <!-- <h1 v-if="graduated">{{ student }}</h1>
    <h1 v-else="graduated">loser</h1>
    <ul>
      <li v-for="animal in animals" :key="animal">{{ animal }}</li>
    </ul>
    <div class="buttons">
      <button @click="authState" v-if="loggedin">Log Out</button>
      <button @click="authState" v-else>Log In</button>
    </div>
    <input type="text" placeholder="edit me" v-model="message" />
    <h3>{{ message }}</h3> -->
  </main>
</template>
