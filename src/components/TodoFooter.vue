<template>
  <div class="footerContainer">
    <div>
      <span class="clearAllBtn" @click="clearAll">Clear All</span>
    </div>
    <div class="waterMark">
      <span>made by RunningWater</span>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    clearAll() {
      this.$emit("removeAll");
    }
  }
};
</script>

<style scoped>
.footerContainer {
  width: 80%;
  margin: 2rem auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.clearAllBtn {
  color: white;
  background-color: red;
  display: inline-block;
  padding: 0.8rem 1rem;
  font-size: 18px;
  font-weight: bold;
}
.waterMark {
  margin-top: 1rem;
}
.waterMark span {
  font-size: 18px;
  font-weight: bold;
  color: #7f8c8d;
}
</style>