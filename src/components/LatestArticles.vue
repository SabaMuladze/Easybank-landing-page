<template>
  <div class="cont">
    <div class="head">
      <h2>Latest Articles</h2>
    </div>
    <div class="article">
      <ul>
        <li v-for="(article, index) in articles" :key="index">
          <img class="articleImg" :src="'/' + article.img" alt="s" />
          <div class="alignment">
            <p>{{ article.by }}</p>
            <h3>{{ article.title }}</h3>
            <p>{{ article.description }}</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          img: "image-currency.jpg",
          by: "by Claire Robinson",
          title: "Receive money in any currency withno fees",
          description:
            "The world is getting smaller and we’re becoming more mobile. So why should you beforced to only receive money in a single …",
        },
        {
          img: "image-restaurant.jpg",
          by: "by Wilson Hutton",
          title: "Treat yourself without worrying about money",
          description:
            "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …",
        },
        {
          img: "image-plane.jpg",
          by: "by Wilson Hutton",
          title: "Take your Easybank card wherever you go",
          description:
            "We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …",
        },
        {
          img: "image-confetti.jpg",
          by: "by Claire Robinson",
          title: "Our invite-only Beta accounts are now live!",
          description:
            "After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site …",
        },
      ],
    };
  },
};
</script>

<style scoped>
.articleImg {
  width: 100%;
  max-height: 200px;
  position: relative;
  top: 0;
  border-radius: 5px;
}
.cont {
  margin: 0 24px;
  min-height: 60vh;
  font-weight: 300;
}
li {
  list-style: none;
  border-radius: 5px;
  box-shadow: 0px 3px 3px 0px rgba(0, 0, 0, 0.1);
  max-width: 300px;
  max-height: 440px;
}
.article {
  display: flex;
  justify-content: center;
}

.alignment {
  display: flex;
  flex-direction: column;
  gap: 13px;
  padding: 30px;
}
ul {
  display: flex;
  flex-direction: column;
  gap: 30px;
  align-items: center;
}
h2 {
  margin-top: 70px;
  margin-bottom: 25px;
  font-size: 30px;
}

@media (min-width: 768px) {
  ul {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    width: fit-content;
    gap: 2.5rem;
  }
}
@media (min-width: 1024px) {
  .cont {
    padding: 0 80px;
  }
  h2 {
    font-size: 36px;
  }
  ul {
    display: flex;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;
  }
  li {
    cursor: pointer;
    transition: 0.3s;
  }
  li:hover {
    scale: 1.1;
  }
}
@media (min-width: 1440px) {
  .head {
    padding-left: 170px;
  }
  ul {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
  }
}
</style>
