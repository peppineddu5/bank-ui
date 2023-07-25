<script lang="ts">
import { ref } from 'vue';
import PrimaryButton from "./secondary/PrimaryButton.vue"
export default {
    setup(){
        const hamActive=ref("");

        function renderImg(path:string) {
          return require('../assets/'+path)
        }
        function setHAmActivation(){
            return hamActive.value==""?hamActive.value="active":hamActive.value=""
        }
        return{
            hamActive,
            renderImg,
            setHAmActivation,
        }
    },
    components:{PrimaryButton}
}
</script>
<template>
    <nav class="navbar">
        <img src="../assets/logo-icon.svg" alt="">
        <ul :class="hamActive">
            <li><a href="#" class="nav-but">Home</a></li>
            <li><a href="#" class="nav-but">About</a></li>
            <li><a href="#" class="nav-but">Contact</a></li>
            <li><a href="#" class="nav-but">Blog</a></li>
            <li><a href="#" class="nav-but">Careers</a></li>
        </ul>

        <PrimaryButton text="Request Invite"/>
        <img @click="setHAmActivation()" :src="hamActive==''?renderImg('icon-hamburger.svg'):renderImg('close-ham.svg')" class="hamburger">
    </nav>
</template>
<style>
.navbar{
    z-index: 2;
    position: fixed;
    width: 100%;
    top: 0;
    padding: 20px 0;
    font-weight: 200;
    background-color: white;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    
}
.navbar ul{
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 31px;
    list-style-type: none;
}

.nav-but{
    color: #9698A6;
    text-decoration: none; 
}
.hamburger{
    cursor: pointer;
    display: none;
    height: 21px;
    width: 24px;
    object-fit: contain;
}
@media only screen and (max-width: 800px){
    .navbar button{
        display: none;
    }
}

@media only screen and (max-width: 650px){
    .navbar{
        justify-content: space-between;
        padding: 20px 30px;
    }
    .navbar button{
        display: none;
    }
    .navbar ul{
        position: fixed;
        background-color: #FAFAFA;
        width: 90%;
        padding: 20px;
        border-radius: 10px;
        color: #9698A6;
        left: 50%;
        margin-top: 20px;
        position: absolute;
        top: 61px;
        flex-direction: column;
        transform: translate(-50%, 0);
        
    }
    .navbar ul{
        display: none;
    }
    .navbar ul.active{
        display: flex;
    }
    .hamburger{
        display: block;
    }
}
</style>