<template>
  <div class="center_from">
    <div class="box">
      <div class="ma">
        <b-button href="#" variant="primary" @click="createtodo"
          >สร้าง todo</b-button
        >
      </div>
      <div class="form-group kan" role="group">
        <div class="m-5">
          <label for="input-live">Name</label>
          <input type="text" class="form-control" v-model="name" />

          <form class="row g-3">
            <label for="todo" class="visually-hidden">todo</label>

            <div class="col-auto">
              <select class="form-select" aria-label="Default select example">
                <option selected>เลือกหมวดหมู่</option>
                <option value="1">หมวดหมู่1</option>
                <option value="2">หมวดหมู่2</option>
                <option value="3">หมวดหมู่3</option>
              </select>
            </div>
            <div class="col-auto">
              <button type="submit" class="btn btn-primary mb-3">ลบ</button>
            </div>
          </form>
          <form class="row g-3">
            <button type="submit" class="btn btn-primary mb-3">เพิ่ม</button>

            <div class="col-auto">
              <select class="form-select" aria-label="Default select example">
                <option selected>เลือกหมวดหมู่</option>
                <option value="1">หมวดหมู่1</option>
                <option value="2">หมวดหมู่2</option>
                <option value="3">หมวดหมู่3</option>
              </select>
            </div>
            <div class="col-auto">
              <button type="submit" class="btn btn-primary mb-3">ลบ</button>
            </div>
          </form>
        </div>
      </div>
    </div>

    <div class="center_box mt-5">
      <div>
        <b-button href="#" variant="primary" @click="back">กลับ</b-button>
      </div>
      <div class="col-md-10"></div>
      <b-button href="#" variant="primary" @click="save">ยืนยัน</b-button>
    </div>
  </div>
</template>

<script>
export default {
  layout: "user",
  data() {
    return {
      name: "",
      lastname: "",
    };
  },
  methods: {
    save() {
      this.$router.push("/category");
    },
    back() {
      this.$router.push("/category");
    },
    categoryat1() {
      this.$router.push("/category/catedit/");
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
  justify-content: space-between;
  align-items: flex-end;
  flex-grow: 1;
  display: flex;
}
.center_from {
  justify-content: center;
  align-items: center;
  flex-grow: 1;
}
.kan {
  min-height: 300px;
  border: 1px solid gray;
  border-radius: 10px;
}
.box {
  margin: auto;
  width: 80%;
  margin-top: 100px;
}
.form-select {
  min-height: 40px;
  border-radius: 5px;
  width: 500px;
}
.row {
  justify-content: space-between;
  margin-top: 15px;
}
</style>

