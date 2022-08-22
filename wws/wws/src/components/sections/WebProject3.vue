<template>
    <section class="web-project-3" id="web-project-3">

        <rotation-layout>
        <template v-slot:face1>
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
        </template>
        </rotation-layout>




    </section>
</template>

<script>

import ProjectPageLayout from "../layout/ProjectPageLayout.vue";
import RotationLayout from "../layout/rotationLayout.vue";

export default {
    components:{
        ProjectPageLayout,
        RotationLayout
    },
    data(){
        return {
            mainTitle : "Web Project 3",
            subTitle: "2019-OPTION KATZE II",
            linkToProjectDescription: "View Project Description",
            projectIconUrl: require('@/assets/img/projects/web_project_3/logo.png'),
            FrontEndTechList: ['HTML/CSS','Javascript'],
            BackEndTechList: ['Python','Django', 'MySQL'],
            DesignStyleList: ['Ajax  for data exchange', 'Bootstrip for styling','JQuery', 'Yahoo-Finance-API for historical stock data'],
            mediaType:"image",
            mediaDisplayUrl: require('@/assets/img/projects/web_project_3/cover.png'),
            backgroundColor:"Black",
            fontColor:"white",
            buttonColor:"#EAAB15",
            projectDescription :"Technical Analysis (TA) is a method to predict the price movement of an asset. But it is always blamed by fundamental investors that TA is nothing but astrology. So, to dig out how accurate TA could be in investment, I made this application for back testing difference TA strategies, to see wether it is really profitable if disciplinarily following the TA strategies,  Yahoo-finance API is used to extract historical price data<br><br>By clicking the  “View Demo” button above, you can see if I buy 0002.hk when RSI is lower than 20 and sell when hight than 70, it in the end is a profitable strategy.  But it doesn’t mean that we can have the same positive result if trying the same strategy on other assets. "
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
.web-project-3{
    width:100vw;
    height: 100vh;
    background-color: rgb(0, 0, 0);
}

</style>