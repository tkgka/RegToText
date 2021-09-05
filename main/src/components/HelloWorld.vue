<template>
  <div class="hello">
    <input value="" v-model="input1" />
    <button @click="gen_val()">Reload</button>
  </div>
</template>

<script lang="ts">
import RandExp from "randexp";

// sets and ranges and references
export default {
  data() {
    return {
      input1: "[a-z]{0,20}",
      //v-show 는 렌더링 함 , v-if는 렌더링 조차 하지 않음
    };
  },

  methods: {
    gen_val() {
      // eslint-disable-next-line
      const generated_val = new RandExp(this.input1).gen();
      alert(generated_val);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
