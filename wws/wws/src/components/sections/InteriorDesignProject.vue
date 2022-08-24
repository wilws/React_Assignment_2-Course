<template>
    <section class="interior-design-project-1" id="interior-design-project-1">
        
        <rotation-layout-5 ref="rotationLayoutRef5">
       
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
            <div class="slot2-wrapper">
                <div class="left-side">
                    <h1>Messy Storage Room</h1>
                    <div class="content">
                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Earum quidem, quam dolore provident eaque debitis laudantium ullam aperiam incidunt eveniet repellendus eos consequatur dicta laboriosam, nostrum porro accusamus nihil. Dolore?
                    </div>
                </div>
                <div class="right-side">
                    <img :src="require('@/assets/img/projects/interior_design_project_1/p1.jpeg')"/>
                </div>
            </div>
        </template>
        <!-- End of slot 2 -->

        <!-- slot 3 -->
        <template v-slot:slot3>
            <div class="slot3-wrapper">
                <div class="col-1">
                    <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p2-1.png')"/></div>
                    <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p2-2.png')"/></div>
                    <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p2-3.png')"/></div>
                </div>
                <div class="col-2">
                    <div class="h1-wrapper">
                        <h1>Messy Storage Room</h1>
                    </div>
                    <div class="content">
                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Earum quidem, quam dolore provident eaque debitis laudantium ullam aperiam incidunt eveniet repellendus eos consequatur dicta laboriosam, nostrum porro accusamus nihil. Dolore?
                    </div>
                </div>
                <div class="col-3">
                    <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p2-4.jpeg')"/></div>
                    <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p2-5.png')"/></div>
                    <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p2-6.png')"/></div>
                </div>

            </div>
        </template>
        <!-- End of slot 3 -->


        <!-- slot 4 -->
        <template v-slot:slot4>
            <div class="slot4-wrapper">
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-1.jpeg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-2.jpeg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-3.jpeg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-4.jpg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-5.jpg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-6.jpg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-7.jpg')"/></div>
                <div class="img"><img :src="require('@/assets/img/projects/interior_design_project_1/p3-8.jpg')"/></div>
                <div class="left-frame">
                    <div class="h1-wrapper">
                        <h1>Messy Storage Room</h1>
                    </div>
                    <div class="content">
                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Earum quidem, quam dolore provident eaque debitis laudantium ullam aperiam incidunt eveniet repellendus eos consequatur dicta laboriosam, nostrum porro accusamus nihil. Dolore?
                    </div>
                </div>
            </div>
        </template>
        <!-- End of slot 4 -->

    








        </rotation-layout-5>
    </section>
</template>

<script>

import ProjectPageLayout from "../layout/ProjectPageLayout.vue";
import RotationLayout5 from "../layout/rotationLayout.vue";
export default {
    components:{
        ProjectPageLayout,
        RotationLayout5
    },
     mounted(){
        // pass proprs to "rotation-layout" slot
        this.$refs.rotationLayoutRef5.buttonSetting = { 
            backgroundColor : "grey",
            color:"White",
        }
        this.$refs.rotationLayoutRef5.boxClass = ".interior-design-project-1 .space .box";
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
            this.$refs.rotationLayoutRef5.rotate('forward');
        }
    }
}
</script>


<style lang="scss" scoped>
.interior-design-project-1{
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

.slot2-wrapper{
    @extend .slot-wrapper;

    .left-side{
        position:absolute;
        // width:30rem;
        width: 25%;
        height:100%;
        top:0;
        left:0;
        // border: thin solid red;
        padding: 4rem;
        @include column-horizontal-center();
        h1{
            // border: thin solid red;
            width:100%;
            text-align: center;
            font-family: $secondary-font;
            font-size: 2.6rem;
            font-weight: 300;
            letter-spacing: .2rem;
            height:25%;
            line-height:20rem;
        }
        .content{
            // border: thin solid red;
            font-family: $primary-font;
            font-size:1.6rem;
            letter-spacing: .2rem;
            width:100%;
            height:75%;
            text-align: center;
        }
    }
    .right-side{
        position:absolute;
        
        top:0;
        right:0;
        width:75%;
        height:100%;
        // width:1365px;
        // border: thin solid red;
        
        img{
            width:100%;
            height:100%;
            object-fit: cover;
            
        }
    }
}


.slot3-wrapper{
    @extend .slot-wrapper;
    padding: 0;
    

    .col-1{
        position:absolute;
        width:30%;
        height:100%;
        left:0;
        top:0;
        @include column-horizontal-center();

        .img{
            width:100%;
            height:100%;
            border: thick black solid;
            img{
                width:100%;
                height:100%;
                object-fit: cover;
            }
        }

        .img:nth-child(1){
            height:30%;
        }
        .img:nth-child(2){
            height:40%;
        }
        .img:nth-child(3){
            height:30%;
        }
    }
    .col-2{
        width:40%;
        height:100%;
        border: .5rem black solid;
        @include column-horizontal-center();
        .h1-wrapper{
            h1{
                width:100%;
                text-align: center;
                font-family: $secondary-font;
                font-size: 2.6rem;
                font-weight: 300;
                letter-spacing: .2rem;
                height:25%;
                line-height:20rem;
            }
        }
        .content{
            font-family: $primary-font;
            font-size:1.6rem;
            letter-spacing: .2rem;
            width:70%;
            height:75%;
            text-align: center;
            padding: 0 10rem;
        }
    }
    .col-3{

        position:absolute;
        width:30%;
        height:100%;
        right:0;
        top:0;
        // @include column-horizontal-center();
        display: flex;
        flex-wrap: wrap;
        .img{
            border: thick black solid;
            img{
                width:100%;
                height:100%;
                object-fit: cover;
            }
        }

        .img:nth-child(1){
            width:100%;
            height:60%;
        }
        .img:nth-child(2){
            width:50%;
            height:40%;
        }
        .img:nth-child(3){
             width:50%;
            height:40%;
        }
    }

}

.slot4-wrapper{
    @extend .slot-wrapper;
    padding:0;
    background-color: black;

    .img{
        position:absolute;
        height:100%;
        width:40%;
        top:0;
        img{
            width:100%;
            height:100%;
            object-fit: cover;
        }
    }

    .img:nth-child(1){
        left:0;
        // opacity:0.2;
    }

    .img:nth-child(2){
        left:6%;
        // opacity:0.2;
    }
    .img:nth-child(3){
        left:14%;
        // opacity:0.2;
    }
    .img:nth-child(4){
        left:21%;
        // opacity:0.2;
    }
    .img:nth-child(5){
        left:29%;
        // opacity:0.2;
    }
    .img:nth-child(6){
        left:38%;
        // opacity:0.2;
    }
    .img:nth-child(7){
        left:43%;
        // opacity:0.2;
    }
    .img:nth-child(8){

        width:50%;
        right:0%;
    }

    .left-frame{
        position:absolute;
        width:50%;
        height:100%;
        left:0;
        top:0;
        background-color: rgba(0, 0, 0, 0.863);
        @include column-horizontal-center();
        color: white;
        .h1-wrapper{
            h1{
                width:100%;
                text-align: center;
                font-family: $secondary-font;
                font-size: 2.6rem;
                font-weight: 300;
                letter-spacing: .2rem;
                height:25%;
                line-height:20rem;
            }
        }
        .content{
            font-family: $primary-font;
            font-size:1.6rem;
            letter-spacing: .2rem;
            width:70%;
            height:75%;
            text-align: center;
            padding: 0 10rem;
        }
    }

}
</style>