<script lang="ts">
import PrimaryButton from "./secondary/PrimaryButton.vue"
export default{
    components:{
        PrimaryButton
    }
}
</script>
<template>
    <div class="hero">
        <div class="hero-text">
            <h1>Next generation <br/>
                digital banking!!!!</h1>
            <p>Take your financial life online. Your Easybank
                account will be a one-stop-shop for spending,
                saving, budgeting, investing, and much more.</p>
                <PrimaryButton text="Request Invite"/>
        </div>
        <div class="hero-img">
            <div></div>
            <img src="../assets/image-mockups.png" class="h-m">
        </div>
    </div>
</template>

<style>
.hero{
    height: 100vh;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: space-between;
}


.hero-img{
    height: 100%;
    z-index: -1;
    position: relative;
    
}
.h-m{
    position: relative;
    left:  120px;
}
.hero-img div{
    position: absolute;
    bottom: 00px;
    left: 0;
}
.hero-img div{
    z-index: -1;
    top: -30px;
    width: 100%;
    height: 100%;
    background-image: url("../assets/bg-intro-desktop.svg");
    background-repeat: no-repeat, no-repeat;
}
.hero-text{
    margin: 0 min(50px,10vw);
}
.hero-text h1{
    padding: 10px 0;
    font-size: 52px;
    color: #2D314D;
    font-weight: 400;
}
.hero-text p{
    padding: 20px 0;

    font-size: 18px;
    color: #9698A6;
    font-weight: 400;
}
.hero-text button{
    margin: 0 10px;
}
@media only screen and (max-width: 727px){
    .hero-img{
        width: 100%;
        display: flex;
        justify-content: center;
        height: 90%;
    }
    .hero-img div{
        background-image: url("../assets/bg-intro-mobile.svg");
        top: 200px;
        background-position: right top;
        
    }
    .h-m{
        height: 80%;
        left:0;
    }
    .hero{
        flex-direction: column-reverse;
    }
    .hero-text{
        position: relative;
        top: -100px;
    }
}
</style>
