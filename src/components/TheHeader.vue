<template >
    <div>
        <header>
        <img src="../assets/images/logo.svg" alt="logo">
        <img :src="outputBurgerPic" @click="changeBurgerPic">
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
        closeBurger: 'src/assets/images/icon-close.svg'
    }
    
},
methods: {
        changeBurgerPic(){
            this.menu = !this.menu
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
.menu{
    margin: 9px 16px 10px 16px;
    background-color: white ;
    border-radius: 10px;
    display: flex;
    justify-content: center;

}
.menu li {
    list-style: none;
}
.pages-p{
    font-size: 24px;
    margin: 10px;
}
</style>