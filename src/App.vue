<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <TodoList></TodoList>
    <TodoFooter></TodoFooter>
  </div>
</template>

<script>
import TodoHeader from "../src/components/TodoHeader";
import TodoInput from "../src/components/TodoInput";
import TodoList from "../src/components/TodoList";
import TodoFooter from "../src/components/TodoFooter";

export default {
  components: {
    TodoHeader: TodoHeader,
    TodoInput: TodoInput,
    TodoList: TodoList,
    TodoFooter: TodoFooter
  }
};
</script>
<style>
body {
  background-color: #f6f6f8;
}
input {
  border-style: groove;
  width: 80%;
}
button {
  border-style: groove;
}
.shadow {
  box-shadow: 5px 10px 10px rgba(0, 0, 0, 0.03);
}
</style>
