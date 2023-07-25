<script lang="ts">
import RealFeature from './secondary/RealFeature.vue';
export default {
    components:{
        RealFeature
    },
    setup(){
        const features=[
            {
                img:"icon-online.svg",
                title:"Online Banking",
                paragra:"Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world."
            },
            {
                img:"icon-budgeting.svg",
                title:"Simple Budgeting",
                paragra:"See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits."
            },
            {
                img:"icon-onboarding.svg",
                title:"Fast Onboarding",
                paragra:"We don’t do branches. Open your account in minutes online and start taking control of your finances right away."
            },
            {
                img:"icon-api.svg",
                title:"Open API",
                paragra:"Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier."
            },
        ]
        return {features}
    }
}
</script>
<template>
    <div class="section-feature">
        <div class="feature-text">
            <h2>Why choose Easybank?</h2>  
            <p>We leverage Open Banking to turn your bank account into your financial hub.<br/>
                Control your finances like never before.</p>  
        </div>

        <div class="feature-show">
            <RealFeature v-for="feature in features" :key="feature.title" :img="feature.img" :title="feature.title" :paragra="feature.paragra"/>
        </div>
    </div>
</template>
<style>
.section-feature{
    min-height: 100vh;
    background-color: #F3F4F6;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 60px;
}
.feature-text{
    padding: 0 min(100px,10vw);
}
.feature-text h2{
    margin-top: 20px;
    color: #2D314D;
    font-size: 36px;
    font-weight: 300;
}
.feature-text p{
    padding: 35px 0;
    color: #9698A6;
    font-weight: 400;
    font-size: 18px;
}
.feature-show{
    padding: 0 min(10px,5vw);
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 30px;
}
@media only screen and (max-width: 500px){
    .feature-show{
        padding: 0 0;
        gap: 18px;
    }
}
</style>