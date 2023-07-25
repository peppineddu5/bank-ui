<script lang="ts">
import PrimaryButton from './secondary/PrimaryButton.vue';
export default {
    components:{
        PrimaryButton
    }
}
</script>

<template>
    <footer>
        <div >
            <img src="../assets/logo-white.svg">
            <ul class="social">
                <li><a href=""><img src="../assets/icon-facebook.svg"></a></li>
                <li><a href=""><img src="../assets/icon-youtube.svg"></a></li>
                <li><a href=""><img src="../assets/icon-twitter.svg"></a></li>
                <li><a href=""><img src="../assets/icon-pinterest.svg"></a></li>
                <li><a href=""><img src="../assets/icon-instagram.svg"></a></li>
            </ul>
        </div>
        <div class="links-footer">
            <ul>
                <li><a href="">About Us</a></li>
                <li><a href="">Contact</a></li>
                <li><a href="">Blog</a></li>
            </ul>
            <ul>
                <li><a href="">Careers</a></li>
                <li><a href="">Support</a></li>
                <li><a href="">Privacy Policy</a></li>
            </ul>
        </div>
        <div class="ultimate-sec-fot">
            <PrimaryButton text="Request Invite"/>
            <span>© EasyBank. All Rights Reserved.</span>
        </div>
    </footer>
</template>

<style>
footer{
    margin-top: 70px;
    padding: 82px 0;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    width: 100%;
    background-color: #2D314D;
}
footer div ul{
    list-style: none;
}
div ul li a{
    color: #FFF;
    font-size: 15px;
    font-weight: 300;
    line-height: 33.75px; 
    text-decoration: none;
}
footer div:first-child{
    align-items: center;
    gap: 30px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.social{
    display: flex;
    gap: 10px;
}
.ultimate-sec-fot{
    gap:30px;
    display: flex;
    flex-direction: column;
}
footer span{
    color: #9698A6;
    font-size: 13px;
    font-weight: 300;
    line-height: 16.9px;
}
.links-footer{
    display: flex;
    gap: 90px;
}
.links-footer ul li{
    margin-top:10px;
}
@media only screen and (max-width: 815px){
    footer{
        flex-direction: column;
        gap: 34px;
    }
    .links-footer{
        gap: 70px;
    }
}
</style>