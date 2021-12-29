
<template>
  <div class="index_container">
    <div class="headbar">
      <label for=" "> หน้าแรก </label>
      <div @click="Isopen = true">
        <i class="fas fa-bars"></i>

        <!-- <button
          calss="bar"
          v-on:click="hamburgerclass = !hamburgerclass"
          v-bind:class="hamburgerclass"
          type="buttonType"
        ></button> -->
      </div>
    </div>
    <div :class="hamburgerclass">
      <div class="closebtn" @click="Isopen = false">
        <i class="fas fa-times"></i>
      </div>
      <li class="menu--bar"><a href="#">HOME</a></li>
      <li class="menu--bar"><a href="#">TODO</a></li>
      <li class="menu--bar"><a href="#">CATEGORY</a></li>
      <li class="menu--bar"><a href="#">LOGOUT</a></li>
    </div>

    <div class="bt" href="#">
      <Nuxt />
    </div>

    <footer class="footer">
      <div class="fooker">
        © footer

        <li class="menu--bar"><a href="#">HOME</a></li>
        <li class="menu--bar"><a href="#">TODO</a></li>
        <li class="menu--bar"><a href="#">CATEGORY</a></li>
        <li class="menu--bar"><a href="#">thisisthemay@gmail.com</a></li>
      </div>
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
        return "menu menu--open";
      } else {
        return "menu";
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
.closebtn {
  position: absolute;
  top: 10px;
  right: 15px;
}

/* .fa-bars {
  font-size: 1.5em;
  color: var(--beige);
  display: block;
  width: 50px;
  height: 50px;
  border: none;
  position: relative;
  z-index: 100;
  appearance: none;
  cursor: pointer;
  outline: none;
  margin-top: 15px;
} */
.bodie {
  padding-right: 50px;
  padding-left: 50px;
}

.menu {
  background-color: var(--krom);
  display: block;
  color: var(--beige);
  top: 0;
  left: 0;
  position: fixed;
  width: 0;
  border-radius: 10px;
  padding-top: 50px;
  bottom: 0;
  z-index: 1000;
  overflow-x: hidden;
  transition: width 0.5s;
}

.menu--open {
  width: 100%;
}
.menu--bar {
  text-decoration: none;
  line-height: 1.6em;
  font-size: 1em;
  padding: 0.5em;
  display: block;
  color: var(--beige);

  display: flex;
  justify-content: center;
}

.bar {
  background-color: var(--beige);
}

.bt {
  display: flex;
  flex-grow: 1;
  padding: 0 50px;
  overflow-x: auto;
}
.hamburger {
  background-color: var(--kam);
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
