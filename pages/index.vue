<template>
  <div class="center_box">
    <div class="btntc">
      <div class="bbutton">
        <b-button href="#" variant="outline-primary " @click="todo"
          >todo</b-button
        >
      </div>
      <div class="bbutton">
        <button href="#" variant="outline-primary" @click="category">
          category
        </button>
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
}
:root {
  --white: #faf0e6;
  --beige: #f0e9d2;
  --kakee: #e6ddc4;
  --kam: #678983;
  --krom: #181d31;
}
.btntc {
  grid-template-columns: 1fr;
  grid-template-rows: repeat(2, 1fr);
  display: grid;
  gap: 10px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
.bbutton {
  background-color: var(--kakee);
}
</style>
