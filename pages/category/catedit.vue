<template>
  <div class="center_from">
    <div class="box">
      <div class="form-group kan" role="group">
        <div class="m-5">
          <label for="input-live">Name:</label>
          <input type="text" class="form-control" v-model="name" />

          <label for="input-live">Lastname:</label>
          <input type="text" class="form-control" v-model="lastname" />
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
</style>
