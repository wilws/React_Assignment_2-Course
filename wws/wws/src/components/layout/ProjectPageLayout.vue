<template>

    <!-- secction -->
    <div class="section" :style="{ color:fontColor, backgroundColor:backgroundColor}">
        <div class="left-wrapper">
            <div class="upper-wrapper">
                <div class="left-side">
                    <h1 v-html="mainTitle"></h1>
                    <h3>{{ subTitle }}</h3>
                    <button :style="{ backgroundColor:buttonColor}" @click="workDisplay">{{ linkToProjectDescription }}</button>
                </div>

                <div v-if="projectIconUrl" class="right-side">
                    <img :src="projectIconUrl" alt="logo">
                </div>
            </div>
            <div class="lower-wrapper">
                <p class="left-side">
                    <span v-html="projectDescription"></span>
                </p>

                <div class="right-side">

                    <div v-if="FrontEndTechList.length > 0">
                        <p class="tech-cat-tittle">Front End</p>
                        <li v-for="(tech, index) in FrontEndTechList" :key="index">
                            {{ tech }}
                        </li>               
                    </div>

                    <div v-if="BackEndTechList.length > 0">
                        <p class="tech-cat-tittle">Back End</p>
                        <li v-for="(tech, index) in BackEndTechList" :key="index">
                            {{ tech }}
                        </li>               
                    </div>

                    <div v-if="DesignStyleList.length > 0">
                        <p class="tech-cat-tittle">Design Style</p>
                        <li v-for="(tech, index) in DesignStyleList" :key="index">
                            {{ tech }}
                        </li>               
                    </div>
                </div>
            </div>
        </div>
        <div class="right-wrapper">
            <div v-if="mediaType == 'video'" class="vidoe">
                <video :key="video" controls loop autoplay>
                    <source :src="mediaDisplayUrl" type="video/mp4">
                </video>
            </div>
            <div v-else class="img">
                <img :src="mediaDisplayUrl" alt="cover">
            </div>
        </div>

    </div>
    <!-- End of section -->
    

</template>


<script>
export default {
    props:[
        'mainTitle',
        'subTitle',
        'linkToProjectDescription',
        'projectIconUrl',
        'projectDescription',
        'FrontEndTechList',
        'BackEndTechList',
        'DesignStyleList',
        'mediaDisplayUrl',
        'mediaType',
        'backgroundColor',
        'fontColor',
        'buttonColor'
    ],

    methods:{
        workDisplay(){
            this.$emit('work-display');
        }
    }
}
</script>

<style lang="scss" scoped>
.section{

    width:100%;
    height:100%;
    @include row-horizontal-center();
    overflow: hidden;

    .left-wrapper{
        padding: 4rem;
        width:calc(100% - $projectRightSideWidth);
        height:100%;
        
        .upper-wrapper{
            display: flex;
            justify-content: space-between;
            height:$projectLeftSideTopSideHeight;
            // border: red thin solid;

            .left-side{
                // border:red thin solid;
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
                button{
                    height:3rem;
                    width:16rem;
                    background-color: black;
                    color:white;
                    text-align: center;
                    border-radius: 1rem;
                    margin-top:.7rem;
                    cursor: pointer;
                    transition: transform .5s;

                    &:hover{
                        transform:scale(1.1);
                    }
                }
            }
            .right-side{
                width:32rem;
                // border:red thin solid;
                img{
                    width:100%;
                }
            }
        }

        .lower-wrapper{
            @include row-horizontal-center();
            position: relative;
            width:100%;
            height: calc(100% - $projectLeftSideTopSideHeight);
            margin-top:1rem;
            // border:rgb(59, 47, 47) thin solid;

            .left-side{
                width:70%;
                height: 100%;
                // border:red thin solid;

                font-family: $primary-font;
                color:$grey ;
                font-size: 1.3rem;
                letter-spacing: .1rem ;
                line-height: 3rem;
                text-align: justify;

            }
            .right-side{
                position:absolute;
                bottom:3rem;
                right:0;
                // border:red thin solid;
                font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
     

                div {
                    margin-top:2rem;
                }

                div .tech-cat-tittle{
                    font-weight: bold;
                    font-size: 1.3rem;
                    text-decoration: underline;
                    text-align: right;
                    letter-spacing: .1rem;
                    margin-bottom:.5rem;

                }
                div li{
                    list-style: none;
                    text-align: right;
                    font-size: 1rem;
                    margin-top:.3rem;
                }
            }


        }
    }
    .right-wrapper{
        width: $projectRightSideWidth;
        height: 100%;
        .vidoe{
            width:100%;
            height: 100%;
            // background:rgb(100, 93, 93);
            text-align: center;
            video{
                height:100%;   
                // width:100%; 
                object-fit: cover;
      
            }
        }

        .img{
            width: 100%;
            height: 100%;

            img{
                height: 100%;
                width:100%;
                object-fit: cover;
            }
        }

      
    }
}

</style>