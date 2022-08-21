<template>

  <div class="container">
    <!-- menu -->


    <index-page></index-page>
    <skill-set-page></skill-set-page>
    <web-project-1></web-project-1>
    <web-project-2></web-project-2>
    <web-project-3></web-project-3>
    <web-project-4></web-project-4>


  </div>


</template>

<script>
import IndexPage from "./components/sections/IndexPage.vue";
import SkillSetPage from './components/sections/SkillSetPage.vue';
import WebProject1 from './components/sections/WebProject1.vue';
import WebProject2 from './components/sections/WebProject2.vue';
import WebProject3 from './components/sections/WebProject3.vue';
import WebProject4 from './components/sections/WebProject4.vue';

export default {
  name: 'App',
  components: {
    IndexPage,
    SkillSetPage,
    WebProject1,
    WebProject2,
    WebProject3,
    WebProject4,
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
  // background:red;
}

section{
  height:100%;
  width:100%;
  // background-color: green;
}

</style>
