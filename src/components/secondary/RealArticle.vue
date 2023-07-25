<script lang="ts">
export default{
    props:{
        img:{required:true,type:String},
        title:{required:true,type:String},
        paragra:{required:true,type:String},
        author:{required:true,type:String},
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
    <div class="feature-article">
        <img :src="renderImg(img)">
        <span>{{ author }}</span>
        <h5>{{title}}</h5>
        <p>{{paragra}}</p>
    </div>
</template>
<style>
.feature-article{
    flex: 0 1 90%;
    display: flex;
    flex-direction: column;
    height: 20%;
    max-width: 300px;
    background-color: white;
    box-shadow: 0px 3px 3px 0px rgba(0, 0, 0, 0.10);
    border-radius: 10px;
}
.feature-article img{
    max-height: 500px;
    width: 100%;
    margin-bottom: 30px;
    border-radius: 5px 5px 0 0;
}
.feature-article span {
    align-self: start;
    color: #9698A6;
    font-size: 14px;
    font-weight: 300;
    line-height: 13px; 
    padding: 0 24px;

}
.feature-article h5{
    padding: 0 24px;
    margin-top: 13px;
    color: #2D314D;
    font-size: 19px;
    font-weight: 400;
    line-height: 20px;
}
.feature-article p{
    padding: 0 24px;
    margin-top: 8px;
    margin-bottom: 40px;
    color: #9698A6;
    font-size: 16px;
    font-weight: 300;
    line-height: 21px;
}
@media only screen and (max-width: 1300px){
    .feature-article{
        align-items: center;
    }
}
</style>