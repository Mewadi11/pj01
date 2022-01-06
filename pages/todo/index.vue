<template>
  <div class="center_box">
    <div class="box">
      <div class="ma">
        <b-button href="#" variant="primary " @click="createtodo"
          >สร้าง todo</b-button
        >
        <b-button href="#" variant="danger" @click="edittodo"
          >แก้ไขtodo</b-button
        >
      </div>
      <div v-if="loading">loading</div>
      <div v-else class="m-2">
        <b-table :items="todos" :fields="fields">
          <template #cell(actions)="row">
            <b-button size="sm" @click="info(row)" class="mr-1">
              แก้ไข
            </b-button>
          </template>
          <template #cell(actions2)="row">
            <b-button size="sm" @click="deleteTodo(row)" class="mr-1">
              ลบ
            </b-button>
          </template>
        </b-table>
      </div>
      <div class="d-flex justify-content-end">
        <div>
          <button
            class="btn btn-outline-info"
            v-if="page != 1"
            @click="delPage"
          >
            ย้อนกลับ
          </button>
          <!-- <label for="" href="#"> {{ page }} </label>
          <button class="btn btn-outline-info" @click="addPage">ถัดไป</button> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Swal from "sweetalert2";
export default {
  layout: "user",
  data() {
    return {
      fields: [
        "name",
        "lastname",
        { key: "actions", label: "" },
        { key: "actions2", label: "" },
      ],
      todos: [],
      page: 1,
      loading: false,
    };
  },
  created() {
    this.fetchData();
  },
  methods: {
    createtodo() {
      this.$router.push("todo/create/");
    },
    edittodo() {
      this.$router.push("todo/edittodo/");
    },
    addPage() {
      this.page += 1;
    },
    delPage() {
      this.page -= 1;
    },
    async fetchData() {
      this.loading = true;
      const res = await axios.get("http://192.168.27.105:3000/todo/");
      this.todos = res.data;
      this.loading = false;
    },
    info(row) {
      this.$router.push("/todo/edit/" + row.item.id);
      console.log(row.item.id);
    },
    async deleteTodo(row) {
      const result = await Swal.fire({
        title: "ลบ?",
        text: "deleted " + row.item.id,
        icon: "info",
        confirmButtonText: "ยืนยัน",
        denyButtonText: `ยกเลิก`,
        showDenyButton: true,
      });
      if (result.isConfirmed) {
        await axios.delete("http://192.168.27.105:3000/todo/" + row.item.id);
        this.fetchData();
      }
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
