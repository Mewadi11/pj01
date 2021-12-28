<template>
  <div class="index_container">
    <div v-bind:class="hamburgerclass" href="#"></div>
    <div class="headbar">
      <label for=" "> หน้าแรก </label>
      <div @click="Isopen = true">
        <i class="fas fa-bars"></i>
      </div>
    </div>
    <div class="bt"><Nuxt /></div>

    <footer class="footer">
      <div class="fooker">© footer</div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Isopen: false,
    };
  },
  computed: {
    hamburgerclass() {
      if (this.Isopen) {
        return "hamburger hamburger--open";
      } else {
        return "hamburger";
      }
    },
  },
  methods: {
    home() {
      this.$router.push("/");
    },
    todo() {
      this.$router.push("todo/");
    },
    category() {
      this.$router.push("/category");
    },
  },
};
</script>

<style>
.index_container {
  min-height: 100vh;
  flex-direction: column;
  display: flex;
}
:root {
  --blue: #6495ed;
  --white: #faf0e6;
  --beige: #f0e9d2;
  --kakee: E6DDC4;
  --kam: #678983;
  --krom: #181d31;
}

.headbar {
  background-color: var(--beige);
  color: var(--krom);
  height: 60px;
  padding-right: 50px;
  padding-left: 50px;
  justify-content: space-between;
  display: flex;
  align-items: center;
}

.fa-bars {
  font-size: 1.5em;
}
.bodie {
  padding-right: 50px;
  padding-left: 50px;
}
.bt {
  display: flex;
  flex-grow: 1;
  padding: 0 50px;
}
.hamburger {
  background-color: var(--krom);
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
}
.hamburger--open {
  width: 100%;
}
.footer {
  background-color: var(--krom);
  color: var(--beige);
  padding: 2.5rem;
  text-align: center;
}
</style>
