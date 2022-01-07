<template>
  <div class="pt">
    <div class="hearder">
      <div class="indexlog">
        <label class="plogin">DIGITAL LIBRARY LOGIN</label>
        <b-button>login</b-button>
      </div>
      <div class="moniter">
        <div class="window">
          ลงชื่อเข้าระบบ
          <div class="logo">
            login

            <div class="fab fa-google"></div>
            <div class="fab fa-facebook"></div>
            <div class="fas fa-phone-square-alt"></div>

            <label for="input-live">Username</label>
            <input type="text m-100" class="form-control" v-model="username" />
            <div class="initem">
              <label for="input-live">Password</label>
              <input
                type="text m-100"
                class="form-control"
                v-model="password"
              />
            </div>
            <b-button>login</b-button>
          </div>
        </div>
      </div>
      <div>
        <footer class="footer">
          <div class="down">
            © footer

            <li class="menu--bar"><a href="#">thisisthemay@gmail.com</a></li>
          </div>
        </footer>
      </div>
    </div>
  </div>
</template>


 
<style>
.pt {
  overflow: inherit;
  z-index: 1;
  display: flex;

  background-color: rgb(255, 255, 255);
  min-width: 100vh;
  min-height: 100vh;
}
.moniter {
  display: flex;
  background-color: rgb(255, 202, 171);
  min-width: 100vh;
  min-height: 100vh;
  margin: 60px;
  border-radius: 50px;
}
@media all and (min-width: 1024px) {
  .moniter {
    margin: 70px;
    border-radius: 50px;
    background-color: rgba(107, 107, 114, 0.822);
  }
}

.indexlog {
  display: flex;
  align-items: center;
  background-color: rgb(241, 226, 139);

  padding: 50px;
  height: 6rem;
  min-width: 100vh;
}
.hearder {
  background-color: blueviolet;
  height: 6rem;
  min-width: 100vh;
}
.plogin {
  color: rgb(28, 36, 71);
  justify-content: space-between;
  align-items: center;
}
.window {
  display: flex;
  background-color: rgb(241, 226, 139);
  align-items: center;
  margin: 50px;
  min-width: 100vh;
}
.item {
  background-color: rgb(241, 139, 215);
  border: 1px solid rgb(3, 3, 3);
}
</style>