<template>
  <NavBar/>
  <HeroBanner/>
  <SectionFeature/>
  <SectionArticle/>
  <SectionFooter/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import NavBar from './components/NavBar.vue';
import HeroBanner from './components/HeroBanner.vue';
import SectionFeature from './components/SectionFeature.vue';
import SectionArticle from './components/SectionArticle.vue';
import SectionFooter from './components/SectionFooter.vue';
export default defineComponent({
  name: 'App',
  components: {
    NavBar,
    HeroBanner,
    SectionFeature,
    SectionArticle,
    SectionFooter
  }
});
</script>

<style>

</style>
