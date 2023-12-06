<template >
    <div>
        <header>
        <img src="../assets/images/logo.svg" alt="logo">
        <img :src="outputBurgerPic" @click="changeBurgerPic">
    </header>
    <div>
        <ul>
            <li>Home</li>
            <li>About</li>
            <li>Contact</li>
            <li>Blog</li>
            <li>Carre</li>
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
}
</style>