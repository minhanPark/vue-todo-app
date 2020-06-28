<template>
  <div>
    <input
      type="text"
      v-model="newTodoItem"
      v-on:keyup.enter="addTodo"
      placeholder="할 일을 입력하세요"
      class="shadow"
    />
    <span v-on:click="addTodo">
      <i class="fa fa-plus"></i>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: ""
    };
  },
  methods: {
    addTodo() {
      if (this.newTodoItem !== "") {
        const value = this.newTodoItem && this.newTodoItem.trim();
        this.$emit("addTodo", value);
        this.clearValue();
      }
    },
    clearValue() {
      this.newTodoItem = "";
    }
  }
};
</script>

<style scoped>
div {
  display: flex;
  justify-content: center;
  align-items: center;
}
input {
  padding: 0.6rem 0.35rem;
  font-size: 18px;
  outline: none;
  border: none;
  background-color: white;
}
span {
  padding: 0.6rem 0.6rem;
  font-weight: bold;
  font-size: 16px;
  outline: none;
  background-color: seagreen;
  margin-left: 0.4rem;
}
i {
  color: white;
}
</style>