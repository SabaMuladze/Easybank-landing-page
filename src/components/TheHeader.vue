<template>
  <div class="cont">
    <header>
      <img class="logo" src="../assets/images/logo.svg" alt="logo" />
      <img class="burger" :src="outputBurgerPic" @click="changeBurgerPic" />
      <button class="btn">Request Invite</button>
    </header>
    <div class="menu" v-if="menu">
      <ul>
        <li><p class="pages-p">Home</p></li>
        <li><p class="pages-p">About</p></li>
        <li><p class="pages-p">Contact</p></li>
        <li><p class="pages-p">Blog</p></li>
        <li><p class="pages-p">Carrers</p></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menu: false,
      burger: "/public/icon-hamburger.svg",
      closeBurger: "/public/icon-close.svg",
      screenWidth: window.innerWidth,
    };
  },
  mounted() {
    window.addEventListener("resize", this.handleResize);
    document.addEventListener("DOMContentLoaded", this.pageLoad);
  },

  methods: {
    changeBurgerPic() {
      this.menu = !this.menu;
    },
    handleResize() {
      if (this.screenWidth >= 1024) {
        this.menu = true;
      }
      this.screenWidth = window.innerWidth;
    },
    pageLoad() {
      this.handleResize();
    },
  },
  computed: {
    outputBurgerPic() {
      return this.menu === false ? this.burger : this.closeBurger;
    },
  },
};
</script>

<style scoped>
.cont {
  position: relative;
  widows: 100%;
  z-index: 100;
}
header {
  display: flex;
  justify-content: space-between;
  padding: 0 32px;
  align-items: center;
  min-height: 60px;
  background-color: white;
}
p {
  color: #9698a6;
}

.logo {
  cursor: pointer;
  transition: 0.3s;
}

.logo:hover {
  scale: 1.1;
}

.burger {
  transition: ease-in 1s;
}
.menu {
  margin: 9px 16px 10px 16px;
  background-color: white;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  transition: ease-in 1s;
  position: absolute;
  width: calc(100% - 32px);
}
.menu li {
  list-style: none;
  cursor: pointer;
}

.pages-p {
  font-size: 24px;
  margin: 10px;
  cursor: pointer;
}

.btn {
  padding: 13px 35px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 50px;
  background: linear-gradient(90deg, #31d35c 0%, #2bb7db 100%);
  border: none;
  color: white;
  cursor: pointer;
  font-weight: 300;
  font-size: 15px;
  transition: 5s;
  display: none;
}
.btn:hover {
  background: linear-gradient(90deg, #2bb7db 0%, #31d35c 100%);
}

@media (min-width: 1024px) {
  .menu ul {
    display: flex;
    gap: 32px;
  }
  .menu {
    width: 60%;
    position: absolute;
    left: 20%;
    top: 12px;
    z-index: 1000;
    margin: 0;
  }
  .pages-p {
    font-size: 14px;
  }

  .burger {
    display: none;
  }
  .btn {
    display: flex;
  }

  li:hover p {
    scale: 1.1;
    color: #2ecc71;
  }
}
</style>
