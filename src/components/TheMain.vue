<template >
   <div class="cont">
<div class="main-pic">
<img class="phones" src="../assets/images/image-mockups.png" alt="">
</div>
<div class="main-article">
<h2>Next generation
digital banking!!!!</h2>
<p>Take your financial life online. Your Easybank
account will be a one-stop-shop for spending,
saving, budgeting, investing, and much more.
</p>
<button class="btn">Request Invite</button>
</div>
   </div>
</template>

<script>
export default{

}
</script>

<style scoped>
.cont{
    display: flex;
    flex-direction: column;
    height: 90vh;
    /* overflow: hidden; */
}
.main-pic{
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url('../assets/images/bg-intro-desktop.svg');
    background-repeat: no-repeat;
    overflow:visible;
    width: 100%;
    background-position: center;
    position: relative;
    top: -80px;
}
.phones{
    position: relative;
    min-width: 300px;
}
/* .main-pic{
    background-image: url('../assets/images/bg-intro-mobile.svg');
    width: 100%;
    height: 300px;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    display: flex;
    justify-content: center;
} */


.main-article{
 padding: 0 30px;
 display: flex;
 flex-direction: column;
 gap: 20px;
 
}

h2{
    font-size: 36.96px;
    font-weight: 300;
    text-align: center;
    margin-top: 20px;
}
p{
    color: #9698A6;
    text-align: center;
}

.btn{
padding: 13px 35px;
border-radius: 50px;
background: linear-gradient(90deg, #31D35C 0%, #2BB7DB 100%);
border: none;
color: white;
cursor: pointer;
font-weight: 300;
font-size: 15px;
transition: 5s;
width: 175px;
margin: 10px auto 0 auto;

}
.btn:hover{
    background: linear-gradient(90deg,#2BB7DB  0%, #31D35C 100%);
}

@media (min-width:768px) {
    .phones{
        /* scale: 0.75; */
    }
    .main-pic{
        top: -150px;
    }
}

@media (min-width:1024px) {
.cont{
    flex-direction: row-reverse;
    flex-grow: 12;
}


.main-article{
    flex:1;
    justify-content: center;
}
}

@media (min-width: 1440px) {
    h2,p{
        width: 500px ;
        text-align:left;
        margin-left: 180px;
    }
    .main-pic{
            right: -200px;

    }
 h2{
    font-size: 52px;
 }
 .btn{
    margin-left: 180px;
 }


}
</style>