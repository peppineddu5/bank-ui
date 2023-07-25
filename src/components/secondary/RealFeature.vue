<script lang="ts">
export default{
    props:{
        img:{required:true,type:String},
        title:{required:true,type:String},
        paragra:{required:true,type:String},
    },
    setup(){
        function renderImg(path:string) {
          return require('../../assets/'+path)
        }
        return{
            renderImg
        }
    }
}
</script>

<template>
    <div class="feature-card">
        <img :src="renderImg(img)">
        <h5>{{title}}</h5>
        <p>{{paragra}}</p>
    </div>
</template>
<style>
.feature-card{
    flex: 0 1 89%;
    display: flex;
    flex-direction: column;
    height: 20%;
    max-width: 300px;
}
.feature-card img{
    height: 100px;
    width: 100px;
    margin-bottom: 50px;
}
.feature-card h5{
    color: #2D314D;
    font-size: 24px;
    font-weight: 300;
    line-height: 27px;
}
.feature-card p{
    margin-top: 36px;
    color: #9698A6;
    font-size: 14px;
    font-weight: 300;
    line-height: 21px;
}
@media only screen and (max-width: 1300px){
    .feature-card{
        align-items: center;
    }
}
</style>