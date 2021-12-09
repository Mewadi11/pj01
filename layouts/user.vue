<template>
  <div class="index_container">
    <div>
      <div class="con-center"></div>
      <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#" @click="home">หน้าหลัก</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <div class="col-md-1"></div>

            <b-button size="sm" class="my-2 my-sm-0" type="submit" @click="todo"
              >todo</b-button
            >
            <div class="col-md-1"></div>

            <b-button
              size="sm"
              class="my-2 my-sm-0"
              type="submit"
              @click="category"
              >category</b-button
            >
          </b-nav-form>
        </b-navbar-nav>
      </b-navbar>
    </div>

    <Nuxt />
  </div>
</template>
<script >
export default {
  methods: {
    home() {
      this.$router.push("/");
    },
    todo() {
      this.$router.push("todo/");
    },
  },
};
</script>
<style scoped>
.index_container {
  min-height: 100vh;
  flex-direction: column;
  display: flex;
}
</style>
