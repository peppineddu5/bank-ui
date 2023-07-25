<script lang="ts">
import RealArticle from './secondary/RealArticle.vue';
export default {
    components:{
        RealArticle
    },
    setup(){
        const features=[
            {
                img:"image-currency.jpg",
                author:"By Claire Robinson",
                title:"Receive money in any currency with no fees",
                paragra:"The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single"
            },
            {
                img:"image-currency.jpg",
                author:"By Claire Robinson",
                title:"Receive money in any currency with no fees",
                paragra:"The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single"
            },
            {
                img:"image-currency.jpg",
                author:"By Claire Robinson",
                title:"Receive money in any currency with no fees",
                paragra:"The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single"
            },
            {
                img:"image-currency.jpg",
                author:"By Claire Robinson",
                title:"Receive money in any currency with no fees",
                paragra:"The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single"
            },
        ]
        return {features}
    }
}
</script>
<template>
    <div class="section-article">
        <div class="article-text">
            <h2>Latest Articles</h2>  
        </div>

        <div class="article-show">
            <RealArticle v-for="feature in features" :key="feature.title" :img="feature.img" :title="feature.title" :paragra="feature.paragra" :author="feature.author"/>
        </div>
    </div>
</template>
<style>
.section-article{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 60px;
}
.article-text{
    padding: 0 min(100px,10vw);
}
.article-text h2{
    margin-top: 20px;
    color: #2D314D;
    font-size: 36px;
    font-weight: 300;
}
.article-text p{
    padding: 35px 0;
    color: #9698A6;
    font-weight: 400;
    font-size: 18px;
}
.article-show{
    padding: 0 min(10px,5vw);
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 30px;
}
@media only screen and (max-width: 500px){
    .article-show{
        padding: 0 0;
        gap: 18px;
    }
}
</style>