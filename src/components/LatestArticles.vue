<template >
    <div class="cont">
        <div>
            <h2>Latest Articles</h2>
        </div>
        <div>
            <ul>

            </ul>
        </div>
    </div>
</template>

<script>
export default{
    data() {
        return {
            articles:[
                {
                    img:'image-currency.jpg',
                    title:"Receive money in any currency withno fees",
                    description:'The world is getting smaller and we’re becoming more mobile. So why should you beforced to only receive money in a single …',
                },
                {
                    img:'image-restaurant.jpg',
                    title:"Treat yourself without worrying about money",
                    description:'Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …',
                },
                {
                    img:'image-plane.jpg',
                    title:"Take your Easybank card wherever you go",
                    description:'We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …',
                },
                {
                    img:'image-confetti.jpg',
                    title:"Our invite-only Beta accounts are now live!",
                    description:'',
                },
            ]
        }
    },
}
</script>

<style scoped></style>