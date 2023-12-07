
<template>
  <the-header></the-header>
  <the-main></the-main>
</template>

<script >
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue'
export default{
  components:{
    TheHeader,
    TheMain
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
  background-color: rgba(255, 255, 255, 0.158);
  width: 100%;
  min-height: 100vh;
}

</style>
