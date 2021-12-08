<template>
  <div class="center_box">
    <div>
      <b-button href="#" variant="primary" @click="todo">todo</b-button>
    </div>
    <div class="col-md-1"></div>
    <b-button href="#" variant="primary" @click="createcategory"
      >category</b-button
    >
  </div>
</template>

<script>
export default {
  layout: "user",
  methods: {
    todo() {
      this.$router.push("/todo");
    },
    createcategory() {
      this.$router.push("todo/create");
    },
  },
};
</script>
<style scoped>
.center_box {
  justify-content: center;
  align-items: center;
  flex-grow: 1;
  display: flex;
}
</style>
