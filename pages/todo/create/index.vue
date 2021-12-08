<template>
  <div class="center_from">
    <div role="group">
      <label for="input-live">Name:</label>
      <b-form-input
        id="input-live"
        v-model="name"
        :state="nameState"
        aria-describedby="input-live-help input-live-feedback"
        placeholder="Enter your name"
        trim
      ></b-form-input>

      <!-- This will only be shown if the preceding input has an invalid state -->
      <b-form-invalid-feedback id="input-live-feedback">
        Enter at least 3 letters
      </b-form-invalid-feedback>

      <!-- This is a form text block (formerly known as help block) -->
      <b-form-text id="input-live-help">Your full name.</b-form-text>
    </div>

    <div class="center_box">
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
  methods: {
    save() {
      this.$router.push("todo/");
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
  justify-content: flex-end;
  align-items: flex-end;
  flex-grow: 1;
  display: flex;
}
.center_from {
  justify-content: center;
  align-items: center;
  flex-grow: 1;
}
</style>
