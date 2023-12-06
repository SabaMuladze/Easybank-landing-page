<template >
    <div class="cont">
        <header>
        <img src="../assets/images/logo.svg" alt="logo">
        <img class="burger" :src="outputBurgerPic" @click="changeBurgerPic">
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
export default{
data() {
    return {
        menu: false,
        burger:'src/assets/images/icon-hamburger.svg',
        closeBurger: 'src/assets/images/icon-close.svg',
        screenWidth: window.innerWidth
    }
    
},
mounted() {
    window.addEventListener('resize', this.handleResize);
    document.addEventListener('DOMContentLoaded', this.pageLoad );
  },
  
methods: {
        changeBurgerPic(){
            this.menu = !this.menu
        },
        handleResize() {
            if (this.screenWidth >= 1024) {
                this.menu = true
            }
      this.screenWidth = window.innerWidth;
      
    },
    pageLoad(){
       this.handleResize()
    }
    },
    computed:{
        outputBurgerPic(){
            return this.menu === false ? this.burger : this.closeBurger 
        }
    }
}
</script>

<style scoped>
.cont{
    position: relative;
}
header{
    display: flex;
    justify-content: space-between;
    padding: 0 32px;
    align-items: center;
    min-height: 60px;
    background-color: white ;
}
p{
    color: #9698A6;
}

.burger{
    transition: ease-in 1s;
}
.menu{
    margin: 9px 16px 10px 16px;
    background-color: white ;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    transition: ease-in 1s;
}
.menu li {
    list-style: none;
}
.pages-p{
    font-size: 24px;
    margin: 10px;
    cursor: pointer;
}

@media (min-width: 1024px) {
.menu ul {
    display: flex;
    gap: 32px;
    
}
.menu{
    width: 70%;
    position: absolute;
    left: 15%;
    top: 12px;
    z-index: 1000;
    margin: 0;
}
.pages-p{
    font-size: 14px;
}

.burger{
    display: none;
}
    
}
</style>