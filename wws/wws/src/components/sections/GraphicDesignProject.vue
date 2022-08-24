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
                <div class="slot2-wrapper">
                    <div class="left-side">
                        <div class="bg-img"><img :src="require('@/assets/img/projects/design_project_1/bg-img.jpeg')"></div>
                        <div class="blackbox">
                            <h1>JOYFUL HOUSE</h1>
                            <h3>- a dream of 5 -</h3>
                            <p>Jason with 4 other friends established Joyful House in 2016. It was their dream to have a shop to endlessly supply sweetness to people all around</p>
                        </div>
                    </div>
                    <div class="right-side">
                        <div class="title">LOGO RE-DESIGN</div>
                        <div class="icon-wrapper">
                            <div class="arrow-wrapper">
                               <i class="fa-solid fa-arrow-right-long"></i>
                            </div>
                            <div class="old-icon"><img :src="require('@/assets/img/projects/design_project_1/old_icon.png')"></div>
                            <div class="new-icon"><img :src="require('@/assets/img/projects/design_project_1/logo.png')"></div>
                        </div>
                        <p>To re-brand the company, the very first step is to have a new logo. There were five balloons in the original logo representing the 5 establishers of the dessert shop. I kept this element and the hexagon shape, fusing them with Japanese minimalism.  The slogan “Sweeten up your life” means  “ life is tough, let my dessert to make life sweeter”</p>
                        <div class="ai-img"><img :src="require('@/assets/img/projects/design_project_1/bg-img-icon.png')"> </div>
                    </div>
 
                </div>
            </template>
            <!-- End of slot 2 -->

            <!-- slot 3 -->
            <template v-slot:slot3>
                <div class="slot3-wrapper">

                    <div class="col col-1">
                        <div class="title-wrapper">
                            <h1 class="title">BOX WITHOUT GLUE</h1>
                            <p>Ancient Chinese/Japanese architecture concept-"Nailless”  always connects to the “embodiment of seamlessness”.  The perfect treasure should be placed in a perfect container. Hence all the parts of the box were gule-less so as to express the idea of “seamlessness”</p>
                        </div>
                        <div class="img"><img :src="require('@/assets/img/projects/design_project_1/draft.png')"></div>
                    </div>

                    <div class="col col-2">
                        <div class="img-wrapper">
                            <div class="img"><img :src="require('@/assets/img/projects/design_project_1/making1.jpeg')"></div>
                            <div class="img"><img :src="require('@/assets/img/projects/design_project_1/prototype.jpeg')"></div>
                            <div class="img"><img :src="require('@/assets/img/projects/design_project_1/prototype.png')"></div>
                        </div>
                        <div class="title-wrapper">
                            <h1 class="title">PROTOTYPE</h1>
                            <p>I use paper to make a prototype in order to test if the design is possible </p>
                        </div>
                   </div>

                    <div class="col col-3">
                        <div class="title-wrapper">
                            <h1 class="title">MANUFACTURING</h1>
                            <p>After testing, I contacted packaging manufacturing in China to manufacturing it. The logo was silver plating making it more elegant.</p>
                        </div>
                        <div class="img-wrapper">   
                            <div class="img"><img :src="require('@/assets/img/projects/design_project_1/finish2.jpg')"></div>
                            <div class="img"><img :src="require('@/assets/img/projects/design_project_1/finish1.jpg')"></div>
                        </div>
                    </div>
                </div>
            </template>
            <!-- End of slot 3 -->
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
.web-graphic-design-project-1{
    background-color: rgb(255, 255, 255);
}

// slot 1
.slot-wrapper{
    position: relative;
    width:100%;
    height:100%;
    padding: 4rem;
    background-color: rgb(255, 255, 255);
    color:rgb(0, 0, 0);
    @include column-horizontal-center(); 
}
// End of slot 1


// slot 2
.slot2-wrapper{
    // border:rgb(243, 10, 10) solid thin;
    @extend .slot-wrapper;

    .left-side{

        // border:rgb(240, 177, 3) solid thin;
        position:absolute;
        top:0;
        left:0;
        width:50%;
        height:100%;

        .bg-img{
            position: absolute;
            // border:rgb(128, 128, 128) solid thin;
            height:100%;
            width:100%;
            
            img{
                border:thin pink solid;
                height:100%;
                width:100%;
                object-fit: cover;
            }
        }

        .blackbox{
          
            width:44rem;
            height:37rem;
            background-color: rgba(0, 0, 0, 0.637);
            color:white;
            text-align: center;
            border:none;
            box-shadow: 1.4rem 1.4rem 1rem rgba(0, 0, 0, 0.37);
            @include child-center;
            // border:rgb(4, 245, 185) solid thin;
          
            h1{
                // border:grey solid thin;
                font-family: $secondary-font;
                margin-top:1rem;
                font-size: 4rem;
                letter-spacing: .4rem;;
            }
            h3{
                // border:grey solid thin;
                letter-spacing: .4rem;;
                font-family: Arial, Helvetica, sans-serif;
                font-weight: 100;
                font-size: 2.25rem;
                margin-top:1rem;
            }
            p{
                // border:grey solid thin;
                font-family: $primary-font;
                margin-top:1rem;
                font-size: 1.8rem;
                letter-spacing: .3rem;
                text-align: left;
                padding:4rem;
                line-height: 3.5rem;
            }
        }

    }

    .right-side{
        // border:rgb(240, 177, 3) solid thin;
        position:absolute;
        top:0;
        right:0;
        width:50%;
        height:100%;
        padding: 2rem;
        @include column-horizontal-center(); 

        .title{
            width:100%;
            padding: 1rem;
            text-align: center;
            font-size: 5rem;
            font-family: Arial, Helvetica, sans-serif;
            font-weight: 600;
            letter-spacing: .3rem;
            
        }
        .icon-wrapper{
            position: relative;
            margin-top:7rem;
            // border:rgb(4, 138, 115) solid thin;
            width:60%;
            display: flex;
            justify-content: space-between;

            .arrow-wrapper{
                // border:grey solid thin;
                @include child-center();
                width:6rem;
                height:6rem;
                // @include child-center();

                i{
                    color:rgba(240, 234, 234, 0.904);
                }
            }
            .old-icon{
                // border:rgb(139, 22, 216) solid thin;  
                width:25%;
                img{
                    width:100%;
                    object-fit: cover;
                }
            }
            .new-icon{
                position: relative;
                // border:rgb(3, 68, 57) solid thin;
                width:30%;
                img{
                    @include child-center();
                    width:100%;
                    object-fit: cover;
                }
            }
        }
        p{
            margin-top: 7rem;
            width: 100%;
            padding: 0rem 1rem;
            // border: rgb(3, 68, 57) solid thin;
            font-family: "Nanum Myeongjo", serif;
            color: rgb(26, 25, 25);
            font-size: 1.8rem;
            text-align: center;
            letter-spacing: 0.1rem;
            line-height: 3.3rem;
        }
        .ai-img{
            position: absolute;
            width:100%;
            height:60%;
            bottom:0rem;
            left:0;
            // border:rgb(3, 68, 57) solid thin;
            text-align: center;
            opacity: .2;
            perspective: 100rem;

            img{
                width:90%;
                height:100%;
                object-fit: cover;
                transform-origin: bottom;
                transform: rotateX(60deg);
            }
        }
    }
}

// End of slot 2



// slot 3
.slot3-wrapper{
    // border:rgb(243, 10, 10) solid thin;
    position: relative;
    width:100%;
    height:100%;
    // padding: 4rem;
    background-color: rgb(255, 255, 255);
    color:rgb(0, 0, 0);
    padding: 3rem;;
    display:flex;

    .col{
        position: relative;
        width:33%;
        height:100%;
        padding:0rem 2rem;
        // border:rgb(243, 10, 10) solid thin;
        @include column-horizontal-center();
        justify-content: space-between;

        .title-wrapper{
            width:100%;
            h1{
                // border:rgb(243, 10, 10) solid thin;
                font-family: Arial;
                font-size: 2.6rem;
                letter-spacing: .4rem;
                width:100%;
                text-align: left;
            }
            p{
                margin-top:1.8rem;
                height:10rem;
                // border:rgb(243, 10, 10) solid thin;
                font-family: $primary-font;
                font-size: 1.25rem;
                letter-spacing: .1rem;
                line-height: 1.9rem;
                width:100%;
                // margin-left:1rem;
                text-align: left;
            }
        }
    }

    .col.col-1{
       //  border:rgb(243, 10, 10) solid thin;

        .img{
            // margin-top:3rem;
            width:100%;
            // border:rgb(243, 10, 10) solid thin;
            img{
                width:100%;
                object-fit: cover;
            }
        }

        &::before{
            content:"";
            position:absolute;
            left:0rem;
            top:0;
            width:100%;
            height:80%;
            border-right:grey thin solid;
            background-color: transparent;
        }
    }

    .col.col-2{
        // border:rgb(243, 10, 10) solid thin;

        .img-wrapper{
            width:100%;
            display: flex;
            flex-wrap: wrap;
            // margin-bottom:3rem;
            // border:rgb(90, 5, 5) solid thin;
        
            .img:nth-child(1){
                width:50%;
                // border:rgb(49, 5, 5) solid thin;
                img{
                    width:100%;
                    height: 100%;
                    object-fit: cover;
                }
            }
            .img:nth-child(2){
                width:50%;
                // border:rgb(11, 75, 148) solid thin;
                img{
                    width:100%;
                    height:100%;
                    object-fit: cover;
                }
            }
            .img:nth-child(3){
                width:100%;
                // border:rgb(243, 10, 204) solid thin;
                img{
                    width:100%;
                    height:100%;
                    object-fit: cover;
                }
            }
        }
         &::before{
            content:"";
            position:absolute;
            left:0rem;
            bottom:0;
            width:100%;
            height:80%;
            border-right:grey thin solid;
            background-color: transparent;
        }
    }

    .col.col-3{
        // border:rgb(243, 10, 10) solid thin;

        .img-wrapper{
            position: relative;
            width:100%;
            height: 80%;
            padding: 10rem;
            // border:rgb(90, 5, 5) solid thin;

            .img:nth-child(1){
                // border:rgb(49, 5, 5) solid thin;
                position:absolute;
                bottom:20rem;
                left:0;
                
                width:80%;

                img{
                    width:100%;
                    height:100%;
                    object-fit: cover;
                }
            }
            .img:nth-child(2){
                // border:rgb(11, 75, 148) solid thin;
                position:absolute;
                right:0;
                bottom:0rem;
                width:40%;
                img{
                    width:100%;
                    height:100%;
                    object-fit: cover;
                }
            }
        }
    }

   
}

// End of slot 3



     
</style>