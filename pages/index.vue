<template>
  <div class="center_box">
    <div class="btn">
      <div class="bbutton">
        <b-button href="#" variant="outline-primary" @click="todo"
          >TODO</b-button
        >
      </div>
      <div class="bcbutton">
        <b-button href="#" variant="outline-primary" @click="category"
          >category</b-button
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: "user",
  methods: {
    todo() {
      this.$router.push("/todo");
    },
    category() {
      this.$router.push("/category");
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
  overflow-x: 80%;
}
.btn {
  display: flex;
  padding: 80%;
  justify-content: space-evenly;
  overflow-x: 80%;
}

.bcbutton a {
  display: flex;
  padding: 50px 60px;
  justify-content: space-evenly;
}
@media all and (min-width: 1024px) {
  .bcbutton a {
    display: flex;
    margin-bottom: 20px;
  }
}

.bbutton a {
  padding: 50px 50px;
  display: flex;

  justify-content: space-evenly;
}

@media all and (min-width: 1024px) {
  .bbutton a {
    margin-bottom: 10px;
  }
}
</style>