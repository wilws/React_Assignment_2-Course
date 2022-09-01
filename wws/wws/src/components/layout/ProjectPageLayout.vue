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
                <div class="content">
                    <p class="left-side">
                        <span v-html="projectDescription"></span>
                    </p>

                    <div class="bottom-side">
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
        </div>
        <div class="right-wrapper">
            <div v-if="mediaType == 'video'" class="vidoe">
                <video :key="video" loop autoplay muted>
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
        'buttonColor',
        'id'
    ],
    mounted(){
        window.addEventListener("scroll",()=>{
            this.contentShow();
        });
    },

    methods:{
        workDisplay(){
            this.$emit('work-display');
        },
         contentShow(){
            // When scroll to Skill set page, trigger cardsRotation()

            const headerMovingItems =  [
                `${this.id} div div.left-wrapper div.upper-wrapper .left-side h1`,
                `${this.id} div div.left-wrapper div.upper-wrapper .left-side h3`,
                `${this.id} div div.left-wrapper div.upper-wrapper .left-side button`,
            ];

            const imgPath = `${this.id} div div.left-wrapper div.upper-wrapper .right-side img`;
            if (document.querySelector(imgPath)){
                headerMovingItems.push(imgPath);
            }
            const content = `${this.id}  div div.left-wrapper div.lower-wrapper div.content`;
            const page = document.querySelector(this.id);
            const travelDistance = window.innerHeight + window.pageYOffset;
            const triggerPoint = page.offsetTop + page.offsetHeight/2;
            
            if (travelDistance > triggerPoint){
                headerMovingItems.forEach((item) => {
                    document.querySelector(item).style.transform= 'translateX(0)';
                });      
                document.querySelector(content).style.opacity = '1';
            } 
        }
    }
}
</script>

<style lang="scss" scoped>
.section{

    width:100%;
    height:100%;
    min-width:320px;
    // min-height:568px;
    @include row-horizontal-center();
    overflow: hidden;



    .left-wrapper{
        padding: 0.2rem;
        width:100%;
        height:100%;
        // border:red thin solid;
        padding:1rem 0rem 0.6rem 1rem;
        @media(min-width:350px){
            padding:1rem 1.5rem 1rem 1.5rem;
        }
        
        @media(min-width:500px){
            padding:1rem 2rem 0.6rem 2rem;
        }

        @media(min-width:1024px)and (max-height:1024px) {
            padding:1rem 1rem 0.6rem 1rem;
            width:70%;

        }
        
        .upper-wrapper{
            display: flex;
            justify-content: space-between;
            height:8rem;
            // max-height:30rem;
            visibility: none;
            // border:blue thin solid;

            .left-side{
                display: flex;
                flex-direction: column;
                justify-content: start;

                // border:red thin solid;
                height:100%;
            
                position: relative;
                width:60%;

                @media(min-width:568px){
                    width:70%;
                }
                @media(min-width:768px){
                    width:70%;
                }
                @media(min-width:1024px){
                    width:60%;
                }

                // border:red thin solid;
                h1{
                    position: relative;
                    width:100%;
                    font-family: $secondary-font;
                    font-size:1.1rem;
                    letter-spacing: 0rem;
                    text-align: left;
                    transform:translateX(-200%);
                    transition: transform 1s;

                    @media(min-width:568px){
                        font-size: 1.4rem;
                    }
                    @media(min-width:768px){
                        font-size: 2.6rem;
                    }

                    @media(min-width:1024px) and (max-height: 1024px){
                        font-size: 1.8rem;
                    }  
                    
                    @media(min-width:1024px) and (min-height: 1024px){
                        font-size: 1.8rem;
                    }  
                }

                h3{
                    position: relative;
                     width:100%;
                     font-size: 0.6rem;
                     font-weight: 500;
                     font-family: $secondary-font;
                     letter-spacing: .1rem;
                     padding-left: .2rem;
                     margin-top:-.1rem;
                     text-align: left;
                    transform:translateX(-200%);
                    transition: transform 1s .1s;
                    

                    @media(min-width:568px){
                        font-size: 0.8rem;
                    }
                    @media(min-width:768px){
                        font-size: 1.2rem;
                    }
                    @media(min-width:1024px) and (max-height: 1024px){
                        font-size: 0.8rem;
                    }
                    @media(min-width:1024px) and (min-height: 1024px){
                        font-size: 1.8rem;
                    }
                }
                button{
                    position: relative;
                    // position:absolute;
                    bottom:-.5rem;
                    left:0;
                    height: 1.2rem;
                    width: 6rem;;
                    color: white;
                    text-align: center;
                    border-radius: 1rem;
                    margin-top: 0.2rem;
                    cursor: pointer;
                    transition: transform 0.5s;
                    font-size: 0.5rem;
                    transform:translateX(-200%);
                    transition: transform 1s .3s;
                    

                    @media(min-width:568px){
                        height: 1.5rem;
                        width: 8.9rem;;
                        font-size:.7rem;
                        min-height: 1.5rem;
                    }

                    @media(min-width:768px){
                        height: 1.8rem;
                        width: 9.5rem;;
                        font-size:.7rem;
                    }
                    @media(min-width:1024px) and (min-height: 1024px){
                        height: 3.2rem;
                        width: 12.7rem;
                        font-size: 1rem;
                    }

                    &:hover{
                        transform:scale(1.1);
                    }
                }
            }
            .right-side{
                width:40%;
                text-align: right;
                padding-right:0.3rem;

                // @media(min-width:1024px) and (max-height: 1024px){
                //     font-size: 35%;
                // }

                @media(min-width:500px){
                    width:30%;
                }
                
                @media(min-width:768px){
                    width:43%;
                }

                @media(min-width:1024px) and (max-height: 1024px){
                    width:30%;
                }
                img{
                     z-index: 0;
                    width:100%;
                    // height:100%;
                    max-width:220px;
                    object-fit: cover;
                    transform:translateX(200%);
                    transition: transform 1s;
                }
            }
        }

        .lower-wrapper{
            position: relative;
            width:calc(100% - 0.2rem);
            height:calc(100% - 5rem);
            margin-top:1rem;
            overflow: hidden;

            @media(min-width:768px){
                height:calc(100% - 11rem);
                margin-top:5rem;
            }

            @media(min-width:1024px){
                height:calc(100% - 13rem);
                margin-top:6rem;
            }

            .content{
                position: relative;
                overflow: auto;
                width:100%;
                height: 100%;
                opacity:0;
                transition:opacity 1s 1s;

                .left-side{

                    overflow: scroll;
                    font-family: $primary-font;
                    // color:white ;
                    font-size: 0.8rem;
                    line-height: 1.7rem;
                    text-align: justify;
      
                    padding-right: 1rem;
                    @media(min-width:768px){
                        font-size: 1rem;
                        line-height: 1.9rem;
                    }
                    @media(min-width:1024px){
                        // font-size: 1.3rem;
                        font-size: 0.9rem;
                    }

                    

                }
                .bottom-side{
                    padding-right: 1rem;
                    // display: flex;
                    // gap:5rem;

                    margin-bottom:4rem;
                    // background-color: white;
                    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
                    @media(min-height:1000px){
                        position:absolute;
                        bottom:2rem;
                        right:0;
                    }
                
                    div {
                        margin-top:2rem;
                    }

                    div .tech-cat-tittle{
                        font-weight: bold;
                        font-size: .8rem;
                        text-decoration: underline;
                        text-align: right;
                        letter-spacing: 0rem;
                        margin-bottom:.5rem;

                    }
                    div li{
                        list-style: none;
                        text-align: right;
                        font-size: .6rem;
                        margin-top:.3rem;
                    }
                }
            }


        }
    }
    .right-wrapper{

        display: none;
        max-width:700px;
        width:50%;
        height: 100%;
        z-index: 2;
        // @media(min-width:1024px) and (max-height:1024px){
        //     display:unset;
        // }

        @media(min-width:1024px) and (max-height:1024px){
            display:unset;
        }
        .vidoe{
            width:100%;
            height: 100%;
            background:rgb(255, 255, 255);
            text-align: right;
            
            video{
                height:100%;   
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