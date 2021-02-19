<template>
  <div class="hello">
    <h1>Hello World, {{ name }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Qun",
    };
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
</style>
