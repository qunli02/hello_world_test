<template>
  <div class="hello">
    <h1>Hello World, {{ name }}</h1>
    <h1>
      {{ count }}
    </h1>
    <button @click="addCount()">count</button>
    <ul>
      <li v-for="(toDo, index) in toDoList" :key="index">
        {{ toDo }}
        <button @click="remove(index)">x</button>
      </li>
    </ul>
    <form>
      <label for="name">Add to list</label>
      <input id="name" v-model="name" />
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Qun",
      count: 0,
      toDoList: ["Asdasd", "sdffgfgfccd", "icbjrekfnreihwehjk"],
    };
  },
  methods: {
    addCount() {
      this.count += 1;
    },
    remove(index) {
      this.toDoList.splice(index, 1);
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
