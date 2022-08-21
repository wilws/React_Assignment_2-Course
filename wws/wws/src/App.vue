<template>

  <div class="container">
    <!-- menu -->


    <!-- section 1-->
    <index-page></index-page>

    <!-- section 2-->
    <skill-set-page></skill-set-page>

    <web-project-1></web-project-1>


  </div>


</template>

<script>
import IndexPage from "./components/sections/IndexPage.vue";
import SkillSetPage from './components/sections/SkillSetPage.vue';
import WebProject1 from './components/sections/WebProject1.vue';

export default {
  name: 'App',
  components: {
    IndexPage,
    SkillSetPage,
    WebProject1
  }
}
</script>

<style lang="scss">

/* Common Style */

* {
    margin:0;
    padding:0;
    outline:none;
    box-sizing:border-box;
    text-decoration:none;
}

html{
    font-size:62.5%;
    scroll-behavior: smooth;
}


.container{
  height:100vh;
  width:100vw;
  background:red;
}

section{
  height:100%;
  width:100%;
  background-color: green;
}

</style>
