<template >
    <div class="cont">
        <div class="heading">
            <h2>Why choose Easybank?</h2>
            <p class="par">We leverage Open Banking to turn your bank
account into your financial hub. Control your
finances like never before.</p>
        </div>
        <div class="reasons">
            <ul class="cards">
                <li v-for="(reason, index) in reasons" :key="reason.title">
                    <div class="card">
                        <img :src="`../public/${reason.img}`" alt="img">
                        <h3>{{ reason.title }}</h3>
                        <p>{{ reason.description }}</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default{
data() {
    return {
        reasons:[
            {
                img:'icon-online.svg',
                title: 'Online Banking',
                description: `Our modern web and mobile applications allow
you to keep track of your finances wherever you
are in the world.`,
            },
            {
                img:'icon-budgeting.svg',
                title: 'Simple Budgeting',
                description: `See exactly where your money goes each
month. Receive notifications when you’re close
to hitting your limits.`,
            },{
                img:'icon-onboarding.svg',
                title: 'Fast Onboarding',
                description: `We don’t do branches. Open your account inminutes online and start taking control of yourfinances right away.`,
            },{
                img:'icon-api.svg',
                title: 'Open API',
                description: 'Manage your savings, investments, pension, andmuch more from one account. Tracking yourmoney has never been easier.'
            },
        ]
    }
},
}
</script>

<style scoped>
.cont{
    background-color: #F3F4F6;
    display: flex;
    flex-direction: column;
    position: relative;
    min-height: 65vh;
    width: 100%;
}

.heading{
    display: flex;
    flex-direction: column;
    gap: 25px;
   padding-top: 115px;
   margin-bottom: 80px;
   align-items: center;
}
.cards{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 30px;
}
li{
    list-style: none;
}

.card{
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    max-width: 300px;
}
p{
    color: #9698A6;
    font-size: 14px;
}
h3{
    font-size: 24px;
    color: #2D314D;
}
h2{
    font-size: 36px;
}
.card p{
 padding: 10% 0;
}
.card img{
    margin-bottom: 20px;
}
.par{
    max-width: 600px;
}

@media (min-width: 1024px) {
    .heading{
        width: 60%;
        align-items: start;
        padding-left: 170px;
    }
    .heading p{
        max-width: 680px;
        font-size: 18px;
    }
    .cards{
        justify-content:center;

    }
    .card{
        text-align: start;
        align-items: start;
    }
    
    .cont{
        padding: 0 80px;
    }
   
}

</style>