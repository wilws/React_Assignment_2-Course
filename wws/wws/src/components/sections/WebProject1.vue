<template>
    <section class="web-project-1">
        <project-page-layout

            :mainTitle = "mainTitle"
            :subTitle = "subTitle"
            :linkToProjectDescription = "linkToProjectDescription"
            :projectIconUrl = "projectIconUrl"
            :projectDescription = "projectDescription"
            :FrontEndTechList = "FrontEndTechList"
            :BackEndTechList = "BackEndTechList"
            :DesignStyleList = "DesignStyleList"
            :mediaDisplayUrl = "mediaDisplayUrl"
            :mediaType = "mediaType"
            :backgroundColor = "backgroundColor"
            :fontColor = "fontColor"
            :buttonColor = "buttonColor"
            @work-display = "workDisplay"

        ></project-page-layout>
    </section>
</template>

<script>

import ProjectPageLayout from "../layout/ProjectPageLayout.vue";

export default {
    components:{
        ProjectPageLayout
    },
    data(){
        return {
            mainTitle : "Web Project 1",
            subTitle: "2022-ELLOW TRADITION",
            linkToProjectDescription: "Go to the Web Page",
            projectIconUrl: require('@/assets/img/projects/web_project_1/logo.png'),
            FrontEndTechList: ['HTML/CSS','Javascript','VueJs/Vue-Cli'],
            BackEndTechList: ['NodeJs / ExpressJs', 'MongoDB'],
            DesignStyleList: ['RESTFul API', 'JWT Authentication','Stripe API Payment Gateway'],
            mediaType:"video",
            mediaDisplayUrl: require('@/assets/img/projects/web_project_1/ellow_video.mp4'),
            // mediaDisplayUrl: '/projects/web_project_1/ellow_video.mp4',
            projectDescription :
                "This is a “just for fun” re-build website. The original website of this company was  build by PHP + AJAX + MySQL <br> <br> In 2014 Autumn after quitting my job, I  spent weeks to learn PHP from books and built up my first e-commerce “Ellow Tradition”. It was an online shop selling interesting cultural goods from all over the world, including Germany smoker , nutcracker,  Japanese Daruma Doll, etc.  It was out of my expectation that the website eventually helped me to get an PHP web developer job in a  radio-control (R/C) hobby Company  - AsiaTees.  I had worked in this company for not more than a month before switching to be a civil servant due to salary consideration.  <br> <br>  Since it was my first time to build a website with plain PHP,  the architecture was so out dated.  In order to refresh my web development skills, I have taken courses, in Udemy,  of Vue.js, modern HTML/CSS, Node.js and construction of responsive website. <br> <br>  I always believe that the key to solidify what have learnt is to get your hand dirty  —  Do your own project ! <br> Therefore, I playfully re-built the website. <br> <br> In this website, Adobe XD was used to draft and design the interface. Vue.js is applied as frontend technology, and Node.js + Express framework with MongoDB are used in backend. Both ends are communicated by RESTful API and JWT is used for authentication. Stripe is adopted for payment gateway.",
            backgroundColor:"White",
            fontColor:"Black",
            buttonColor:"Black"
       }
    },
    methods:{
        workDisplay(){
            window.open("https://ellowtradition-vue.herokuapp.com/", '_blank');
        }
    }
}
</script>


<style lang="scss" scoped>
.web-project-1{
    background-color: white;
}

</style>