<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in todos" :key="index">{{ index }}. {{ data.todo }}</li>
      </ul>
      <p v-if="todos.length >= 1">You have more than 1 todo</p>
      <p v-else>You have less than or equal to 1 todo</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Todos',
  data() {
    return {
      todos: [
        { "todo": "buy things"},
        { "todo": "by more fings"},
      ]
    }
  }
}
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
