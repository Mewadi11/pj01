<template>
  <div class="center_box">
    <div class="box">
      <div class="ma">
        <b-button href="#" variant="primary" @click="createtodo"
          >สร้าง todo</b-button
        >
      </div>
      <div class="m-3">
        <b-table :items="todos" :fields="fields"></b-table>
      </div>
      <div class="d-flex justify-content-end">
        <div>
          <button v-if="page != 1" @click="delPage">-1</button>
          <label for="">{{ page }}</label>
          <button @click="addPage">+1</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  layout: "user",
  data() {
    return {
      fields: ["id", "title"],
      todos: [],
      page: 1,
    };
  },
  created() {
    this.fetchData();
  },
  methods: {
    createtodo() {
      this.$router.push("todo/create/");
    },
    addPage() {
      this.page += 1;
    },
    delPage() {
      this.page -= 1;
    },
    async fetchData() {
      const res = await axios.get(
        "http://jsonplaceholder.typicode.com/todos?_start=" +
          (this.page - 1) * 5 +
          "&_limit=5"
      );
      this.todos = res.data;
    },
  },
  watch: {
    page(val) {
      this.fetchData();
    },
  },
};
</script>
<style scoped>
.red {
  background-color: red;
}

.index_container {
  min-height: 100vh;
  flex-direction: column;
  display: flex;
}

.center_box {
  /* justify-content: flex-end; */
  /* align-items: start; */
  flex-grow: 1;
  display: flex;
  padding-left: 50px;
  padding-right: 50px;
}

.box {
  width: 100%;
}
.ma {
  margin-top: 30px;
  text-align: center;
  justify-content: flex-end;
  display: flex;
}
</style>
