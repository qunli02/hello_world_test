<template>
  <div class="hello">
    <h1>Hello World, {{ name }}</h1>
    <h1>
      {{ count }}
    </h1>
    <button @click="addCount()">count</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Qun",
      count: 0,
    };
  },
  methods: {
    addCount() {
      this.count += 1;
    },
  },
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-size: 190px;
}
button {
  font-size: 100px;
  padding: 50px;
}
</style>
