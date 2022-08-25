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
                    <h1>A Messy Storage Room</h1>
                    <div class="content">
                        The place that we rented was used as a store room by the owner.
                        <br>
                        <br>
                        Dusty, scraped wall, worn carpet, dirty window and full of miscellaneous stuff, we were at first in question that was it really possible to use this place as our private harbour?
                        <br>
                        <br>
                        We started to study different information to learn how to do renovation. Finally we found that it was not as difficult as we though
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
                        <h1>Planning</h1>
                    </div>
                    <div class="content">
                        After acquiring knowledge from Internet, YouTube, books..etc, We roughly understood how to do plastering, construction of wooden structure, light and electricity stuff (well..yes...we knew it is dangerous...but we both are graduated from science background and believed in our knowledge. Don’t try it by yourself at home=) ).
                       <br>
                       <br>
                       Having ensured that the renovation was within our ability, I started to learn how to use the software "SketchUp" to draw the layout. 
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

                <div class="complete-wrapper">
                    <div class="left-side">
                        <h1> Desire , Knowledge and Action</h1>
                        <div class="content">
                            We finally spent 3 months to have our cozy studio completed. The whole process was so painful but the outcome was so satisfactory.
                            <br>
                            <br>
                                This experience is so unforgettable. We started from zero, from doubt. We had no knowlege of renovation in the very beginning. But, desire motivated us to pursue knowledge to make it real.
                            <br>
                            <br>
                            "Knowledge" and "Willingness to Learn" provide us confidence to action, to try and to achieve different things in life. Learning endlessly will turn every chapter of your life journey into an exciting adventrue. The more I learn, the more experience that I can put into my life story. We are the sole writer of our life story. Never, Never, Never write a boring story. You don't have another chance to re-write again.
                        </div>
                    </div>
                    <div class="right-side">
                        <img :src="require('@/assets/img/projects/interior_design_project_1/p3-8.jpg')"/>
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
            projectDescription :
            "In Hong Kong, it is quite hard to get a private place for relax since rental is so high in this tiny place. In 2015,  My friend ,Berry ,and I were so luckily to have a chance to rent a place in a factory area with a very economic price. However,  as mentioned, it was in a factory area, the place was “not fancy”, or be more accurate — “messy”. Let see how we 2 turned a messy store room to a cozy studio."







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
            font-size: 2.3rem;
            font-weight: 300;
            letter-spacing: .2rem;
            height:25%;
            line-height:20rem;
        }
        .content{
            // border: thin solid red;
                font-family: $primary-font;
                color:$grey ;
                font-size: 1.3rem;
                letter-spacing: .1rem ;
                line-height: 3rem;
                text-align: justify;
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
        // border-top: 1rem black solid;
        // border-bottom: 1rem black solid;
        @include column-horizontal-center();
        .h1-wrapper{
            h1{
                // border: thin solid red;
                width:100%;
                text-align: center;
                font-family: $secondary-font;
                font-size: 2.3rem;
                font-weight: 300;
                letter-spacing: .2rem;
                height:25%;
                line-height:20rem;
            }
        }
        .content{
            width:60%;
            font-family: $primary-font;
            color:$grey ;
            font-size: 1.3rem;
            letter-spacing: .1rem ;
            line-height: 3rem;
            text-align: justify;
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

    .complete-wrapper{
        position:absolute;
        left:0;
        right:0;
        background-color: rgba(0, 0, 0,0.94);
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        height: 100%;

    
        .left-side{
            // position:relative;
            // background-color: rgba(0, 0, 0, 0.712);
            color: white;
            width: 50%;
            height:100%;
            // border: thin solid red;
            padding: 10rem;
            margin-left:8rem;
            @include column-horizontal-center();
            h1{
                // border: thin solid red;
                width:100%;
                text-align: center;
                font-family: $secondary-font;
                font-size: 2.3rem;
                font-weight: 300;
                letter-spacing: .2rem;
                height:25%;
                line-height:20rem;
            }
            .content{
                // border: thin solid red;
                font-family: $primary-font;
                color:$grey ;
                font-size: 1.3rem;
                letter-spacing: .1rem ;
                line-height: 3rem;
                text-align: center;
                width:100%;
                // padding: 10rem;
            }
        }
        .right-side{
            background-color: rgba(0, 0, 0, 0.562);
            width:40%;
            height:100%;
            // border: thin solid red;
            
            img{
                width:100%;
                height:100%;
                object-fit: cover;
            }
        }
    }

}
</style>