
<template>
  <the-header></the-header>
  <the-main></the-main>
  <why-choose></why-choose>
  <latest-articles></latest-articles>
  <Footer></Footer>

</template>

<script >
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import WhyChoose from './components/WhyChoose.vue';
import LatestArticles from './components/LatestArticles.vue';
import Footer from './components/footer.vue';
export default{
  components:{
    TheHeader,
    TheMain,
    WhyChoose,
    LatestArticles,
    Footer
  }
}
</script>

<style >
@import url('https://fonts.googleapis.com/css2?family=Libre+Franklin:wght@300;600;700&family=Public+Sans:wght@500&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Libre Franklin', sans-serif;
font-family: 'Public Sans', sans-serif;
}
body{
  background-color:  #FAFAFA;;
  width: 100%;
  min-height: 100vh;
  background-image: url('../assets/images/bg-intro-mobile.svg');
  background-size: 800px 700px;
}



</style>
