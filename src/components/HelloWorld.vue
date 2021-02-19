<template>
  <div class="hello">
    <h1>Hello World, {{ name }}</h1>
    <h1>
      {{ count }}
    </h1>
    <button @click="addCount()">count</button>
    <form @submit.prevent="onSubmit(item)">
      <label for="item">Add to list</label>
      <input id="item" v-model="item" />
      <input class="button" type="submit" value="Submit" />
    </form>
    <ul v-if="toDoList.length">
      <li v-for="(toDo, index) in toDoList" :key="index">
        {{ toDo }}
        <button @click="remove(index)">x</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Qun",
      count: 0,
      toDoList: [],
    };
  },
  methods: {
    addCount() {
      this.count += 1;
    },
    remove(index) {
      this.toDoList.splice(index, 1);
    },
    onSubmit(item) {
      this.toDoList.push(item);
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
