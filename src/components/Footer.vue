<template>
  <footer>
    <div class="logo-icons">
      <img src="../assets/images/logo-footer.svg" alt="" />
      <ul>
        <li v-for="(icon, index) in icons" :key="index">
          <a :href="icon.src" target="_blank"
            ><img :src="'./public' + icon.img" alt="icon"
          /></a>
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
          src: "https://www.facebook.com/",
        },
        {
          img: "/icon-youtube.svg",
          src: "https://www.youtube.com",
        },
        {
          img: "/icon-twitter.svg",
          src: "https://www.X.com",
        },
        {
          img: "/icon-pinterest.svg",
          src: "https://www.pinterest.com",
        },
        {
          img: "/icon-instagram.svg",
          src: "https://www.instagram.com",
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
.pages-ul a:hover {
  color: #2ecc71;
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
.btn:hover {
  background: linear-gradient(90deg, #2bb7db 0%, #31d35c 100%);
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
@media (min-width: 1024px) {
  footer {
    flex-direction: row;
    justify-content: space-between;
    padding: 80px 160px;
  }
  .pages-cont {
    flex-direction: row;
    gap: 100px;
  }
  .btn-rights {
    margin-top: 0;
  }
  .pages-ul {
    text-align: start;
  }
}
</style>
