<template>
    <section class="graphic-design-project-1" id="graphic-design-project-1">
        
        <rotation-layout-4 ref="rotationLayoutRef4">

            <!-- slot 1 -->
            <template v-slot:slot1>
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
            <!-- End of slot 1 -->

            <!-- slot 2 -->
            <template v-slot:slot2>
                <div class="slot-wrapper">
                    <div class="title-wrapper">
                        <div class="title">
                            <h1 v-html="mainTitle"></h1>
                            <h3>{{ subTitle }}</h3>
                        </div>
                    </div>
                    <div class="content-wrapper">

                    </div>
                </div>
            </template>
            <!-- End of slot 2 -->


            <!-- slot 3 -->
            <template v-slot:slot3>
                <div class="slot-wrapper">
                    <div class="title-wrapper">
                        <div class="title">
                            <h1 v-html="mainTitle"></h1>
                            <h3>{{ subTitle }}</h3>
                        </div>
                    </div>
                    <div class="content-wrapper">

                    </div>
                </div>
            </template>
            <!-- End of slot 2 -->
        </rotation-layout-4>



    </section>
</template>

<script>

import ProjectPageLayout from "../layout/ProjectPageLayout.vue";
import RotationLayout4 from "../layout/rotationLayout.vue";

export default {
    components:{
        ProjectPageLayout,
        RotationLayout4
    },
    data(){
        return {
            mainTitle : "Graphic and Packaging Design Project",
            subTitle: "2019 - JOYFUL HOUSE",
            linkToProjectDescription: "View Design Work",
            projectIconUrl: require('@/assets/img/projects/design_project_1/logo.png'),
            FrontEndTechList: [],
            BackEndTechList: [],
            DesignStyleList: [],
            mediaType:"image",
            mediaDisplayUrl: require('@/assets/img/projects/design_project_1/cover.jpeg'),
            backgroundColor:"White",
            fontColor:"Black",
            buttonColor:"grey",
            projectDescription :"In the spring of 2019,  My friend Jason was struggling in his cake shop business.  Since the rent of Hong Kong is ridiculously high, he planned to switch the business mode from physical dessert shop to online cake shop.  He asked my assistance to transform the image of the shop. I accepted this challenge with alacrity.<br><br>I first use Adobe Photoshop and Illustrator to re-design the shop logo.  I adopt Japanese minimalism design style. Second, to make the brand on the high-end-track, I designed a “glue-less” cake container. Like ancient Chinese/ Japanese interlocking architecture concept,  “Nailless” in construction is the embodiment of seamlessness."
        }
    },
    mounted(){
        // pass proprs to "rotation-layout" slot
        this.$refs.rotationLayoutRef4.buttonSetting = { 
            backgroundColor : "Grey",
            color:"White",
        }
        this.$refs.rotationLayoutRef4.boxClass = ".graphic-design-project-1 .space .box";
    },
    methods:{
        workDisplay(){
            this.$refs.rotationLayoutRef4.rotate('forward');
        }
    }
}
</script>


<style lang="scss" scoped>
.web-graphic-design-project-1-1{
    background-color: rgb(255, 255, 255);
}


.slot-wrapper{
    position: relative;
    width:100%;
    height:100%;
    padding: 4rem;
    background-color: rgb(255, 255, 255);
    color:rgb(0, 0, 0);
    @include column-horizontal-center();

    .title-wrapper{
        width:100%;

        .title{
            h1{
                width:100%;
                font-family: $secondary-font;
                font-size:4rem;
                letter-spacing: .1rem;
                text-align: left;
            }
            h3{
                width:100%;
                font-size: 2.1rem;
                font-weight: 500;
                font-family: $secondary-font;
                letter-spacing: .2rem;
                padding-left:.4rem;
                margin-top:-.5rem;
                text-align: left;
            }
        }
    }

    .content-wrapper{
        width:100%;
        height: 80%;
        margin-top:5rem;
        text-align: center;

        video{
            height: 100%;
            // width:100%;
            object-fit:cover;
        }
    }
}

</style>