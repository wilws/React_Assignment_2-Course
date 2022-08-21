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
            mainTitle : "Interior Design Project",
            subTitle: "2015 - Studio Design",
            linkToProjectDescription: "View Design Work",
            projectIconUrl: "",
            FrontEndTechList: [],
            BackEndTechList: [],
            DesignStyleList: [],
            mediaType:"image",
            mediaDisplayUrl: require('@/assets/img/projects/interior_design_project_1/cover.jpg'),
            backgroundColor:"White",
            fontColor:"Black",
            buttonColor:"grey",
            projectDescription :"In the spring of 2019,  My friend Jason was struggling in his cake shop business.  Since the rent of Hong Kong is ridiculously high, he planned to switch the business mode from physical dessert shop to online cake shop.  He asked my assistance to transform the image of the shop. I accepted this challenge with alacrity.<br><br>I first use Adobe Photoshop and Illustrator to re-design the shop logo.  I adopt Japanese minimalism design style. Second, to make the brand on the high-end-track, I designed a “glue-less” cake container. Like ancient Chinese/ Japanese interlocking architecture concept,  “Nailless” in construction is the embodiment of seamlessness."
        }
    },
    methods:{
        workDisplay(){
            window.open("http://http://www.longlifeproduction.com", '_blank');
        }
    }
}
</script>


<style lang="scss" scoped>
.web-project-1{
    background-color: rgb(0, 0, 0);
}

</style>