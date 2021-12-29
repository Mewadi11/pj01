<template>
  <div class="center_box">
    <div class="bt">
      <div class="bcbutton">
        <b-button href="#" variant="primary" @click="todo">TODO</b-button>
      </div>
      <div class="bbutton">
        <b-button href="#" variant="primary" @click="category"
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
  overflow-x: 80%;
}
.bt {
  display: flex;
  padding: 80%;
  justify-content: space-evenly;
  overflow-x: 80%;
}

.bcbutton a {
  padding: 50px 50px;
}
@media all and (min-width: 1024px) {
  .bcbutton a {
    margin-bottom: 10px;
  }
}

@media all and (min-width: 1024px) {
  .bbutton a {
    margin-bottom: 10px;
  }
}
.bbutton a {
  padding: 50px 50px;
}
</style>