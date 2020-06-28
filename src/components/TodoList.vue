<template>
  <section>
    <ul>
      <li v-bind:key="todoItem" v-for="(todoItem,index) in propsdata" class="shadow">
        <div>
          <i class="fa fa-check checkBtn"></i>
          {{todoItem}}
        </div>
        <span class="removeBtn" @click="removeTodo(todoItem, index)">
          <i class="fa fa-trash-o"></i>
        </span>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  props: ["propsdata"],
  methods: {
    removeTodo(todoItem, index) {
      this.$emit("removeTodo", todoItem, index);
    }
  }
};
</script>

<style scoped>
ul {
  list-style-type: none;
  width: 70%;
  margin: 2rem auto;
  padding: 1rem 0.7rem;
}
li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 1.2rem;
  background-color: white;
  margin-bottom: 0.6rem;
  padding: 0.6rem 0.35rem;
  border-top-right-radius: 12px;
  border-bottom-left-radius: 12px;
}
.checkBtn {
  font-size: 20px;
  color: green;
}
.removeBtn {
  font-size: 20px;
  color: red;
  padding: 0.1rem;
  cursor: pointer;
}
</style>