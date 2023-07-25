<script lang="ts">
export default{
    props:{
        text:{
            required:true,
            type:String
        },
    }
}
</script>

<template>
    <button class="primary-button">{{ text }}</button>
</template>
<style>
.primary-button{
    color: white;
    padding: 13px 35px;
    border-radius: 50px;
    border: none;
    cursor: pointer;
    background: linear-gradient(90deg, #31D35C 0%, #2BB7DB 100%);
}
</style>