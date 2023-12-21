<template>
  <footer>
    <div class="logo-icons">
      <img src="../assets/images/logo-footer.svg" alt="" />
      <ul>
        <li v-for="(icon, index) in icons" :key="index">
          <img :src="'./public' + icon.img" alt="icon" />
        </li>
      </ul>
    </div>
    <div class="pages-cont">
      <div>
        <ul class="pages-ul">
          <li v-for="(page, index) in pages1" :key="index">
            <a href="#">{{ page.title }}</a>
          </li>
        </ul>
      </div>
      <div>
        <ul class="pages-ul">
          <li v-for="(page, index) in pages2" :key="index">
            <a href="#">{{ page.title }}</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="btn-rights">
      <button class="btn">Request Invite</button>
      <p>© EasyBank. All Rights Reserved.</p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      icons: [
        {
          img: "/icon-facebook.svg",
        },
        {
          img: "/icon-youtube.svg",
        },
        {
          img: "/icon-twitter.svg",
        },
        {
          img: "/icon-pinterest.svg",
        },
        {
          img: "/icon-instagram.svg",
        },
      ],
      pages1: [
        {
          title: "About Us",
        },
        {
          title: "Contact",
        },
        {
          title: "Blog",
        },
      ],
      pages2: [
        {
          title: "Careers",
        },
        {
          title: "Support",
        },
        {
          title: "Privacy Policy",
        },
      ],
    };
  },
  created() {},
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
footer {
  background: #2d314d;
  max-height: 620px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  padding: 40px;
}
ul {
  display: flex;
  gap: 20px;
  justify-content: center;
}
.pages-ul {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-top: 15px;
  text-align: center;
}
li {
  list-style: none;
}
.logo-icons {
  display: flex;
  flex-direction: column;
  gap: 35px;
}
.pages-cont {
  display: flex;
  flex-direction: column;
}
a {
  text-decoration: none;
  color: white;
}
.btn {
  padding: 13px 35px;
  border-radius: 50px;
  background: linear-gradient(90deg, #31d35c 0%, #2bb7db 100%);
  border: none;
  color: white;
  cursor: pointer;
  font-weight: 300;
  font-size: 15px;
  width: 175px;
  margin: 10px auto 20px auto;
}
.btn-rights {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 30px;
}
.btn-rights p {
  color: #9698a6;
}
</style>
