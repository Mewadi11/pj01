<template>
  <div class="center_box">
    <div class="col-md-1"></div>
    <b-button href="#" variant="primary" @click="createcategory"
      >สร้างหมวดหมู่</b-button
    >
  </div>
</template>

<script>
export default {
  layout: "user",
  methods: {
    category() {
      this.$router.push("/category");
    },
    createcategory() {
      this.$router.push("category/create");
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
