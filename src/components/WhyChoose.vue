<template >
    <div class="cont">
        <div class="heading">
            <h2>Why choose Easybank?</h2>
            <p>We leverage Open Banking to turn your bank
account into your financial hub. Control your
finances like never before.</p>
        </div>
        <div class="reasons">
            <ul>
                <li v-for="(reason, index) in reasons" :key="reason.title">
                    <div>
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
    min-height: 100vh;
    width: 100%;
}

.heading{
    display: flex;
    flex-direction: column;
    text-align: center;
    gap: 25px;
   padding-top: 115px;
}
</style>