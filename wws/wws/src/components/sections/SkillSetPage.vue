<template>
    <section class="skill-set-page" id="skill-set-page">

        <h1>Skill Set</h1>
        <h3>Here are the programming languages and<br>
        software that I used to create web project. </h3>

        <div class="card-switcher">
            <button @click="moveCard(0)">Frontend</button>
            <button @click="moveCard(1)">Backend</button>
            <button @click="moveCard(2)">Database</button>
            <button @click="moveCard(3)">Others</button>
        </div>

        <!-- <div class="cards-wrapper-vertical-positioner"> -->

            <div class="cards-wrapper">


                <!-- card 1 Front End-->
                <div class="card-wrapper">
                    <div class="card" id="front-end-card">
                        <div class="card-title">
                            <h3>FRONTEND</h3>
                            <h4>TECHNIQUES</h4>
                        </div>

                        <!-- technology used -->

                        <div class="card-tech-chart">

                            <!-- Front-End-1 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Html-five-02.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">HTML</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="html-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Front-End-1 -->

                            <!-- Front-End-2 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/CSS-3-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">CSS / SASS </div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="css-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Front-End-2 -->


                            <!-- Front-End-3 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Javascript-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Javascript</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="javascript-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Front-End-3 -->

                            <!-- Front-End-4 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Vue-js-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Vue.js</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="vuejs-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Front-End-4 -->

                            <!-- Front-End-5 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/React-02.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">React.js</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="reactjs-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Front-End-5 -->
                        


                        </div>
                        <!-- end of technology used -->
                    </div>
                    <!-- End of card -->
                </div>
                <!-- End of card 1 -->

                <!-- card 2 Back End -->
                <div class="card-wrapper">
                    <div class="card" id="front-end-card">
                        <div class="card-title">
                            <h3>BACKEND</h3>
                            <h4>TECHNIQUES</h4>
                        </div>

                        <!-- technology used -->
                        <div class="card-tech-chart">

                            <!-- Back-End-1 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Python-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Python</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="python-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Back-End-1 -->

                            <!-- Back-End-2 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Django-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Django</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="django-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Back-End-2 -->


                            <!-- Back-End-3 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Node-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">NodeJs</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="nodejs-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Back-End-3 -->

                            <!-- Back-End-4 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Express-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">ExpressJs</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="expressjs-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Back-End-4 -->

                            <!-- Back-End-5 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Php-02.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">PHP</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="php-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Back-End-5 -->


                            <!-- Back-End-6 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Laravel-02.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Laravel</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="laravel-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Back-End-6 -->
                        
                        </div>
                        <!-- end of technology used -->
                    </div>
                    <!-- End of card -->
                </div>
                <!-- End of card 2 -->



                <!-- card 3 Database -->
                <div class="card-wrapper">
                    <div class="card" id="front-end-card">
                        <div class="card-title">
                            <h3>DATA BASE</h3>
                            <h4>MANAGEMENT</h4>
                        </div>

                        <!-- technology used -->
                        <div class="card-tech-chart">

                            <!-- Database-1 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Mysql-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">MySQL</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="mysql-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Database-1 -->

                            <!-- Database-2-->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon"  :src="require('@/assets/img/logos/MongoDBLogo.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">MongoDB</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="mongodb-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Database-2 -->
                        
                        </div>
                        <!-- end of technology used -->
                    </div>
                    <!-- End of card -->
                </div>
                <!-- End of card 3 -->


                <!-- card 4 Others -->
                <div class="card-wrapper">
                    <div class="card" id="front-end-card">
                        <div class="card-title">
                            <h3>OTHERS</h3>
                            <!-- <h4></h4> -->
                        </div>

                        <!-- technology used -->
                        <div class="card-tech-chart">

                            <!-- other-1 -->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" style="width:70%" :src="require('@/assets/img/logos/Solidity_logo.svg.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Solidity</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="solidity-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Database-1 -->

                            <!-- other-2-->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Adobe-indesign-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Adobe InDesign</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="indesign-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Database-2 -->

                            <!-- other-3-->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Adobe-_xd_icon.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Adobe XD</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="xd-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of other-3 -->

                            <!-- other 4--->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Adobe-illustrator-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Adobe Illustrator</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="illustrator-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of other-4 -->


                            <!-- other 5--->
                            <div class="tech-wrapper">
                                <div class="left-side">
                                    <img class="tech-icon" :src="require('@/assets/img/logos/Adobe-photoshop-01.png')">
                                </div>
                                <div class="right-side">
                                    <div class="tech-name">Adobe PhotoShop</div>
                                    <div class="tech-bar-wrapper">
                                        <div class="bar" id="photoshop-bar"></div>
                                    </div>
                                </div>
                            </div>
                            <!-- End of Other-5 -->
                        
                        </div>
                        <!-- end of technology used -->
                    </div>
                    <!-- End of card -->
                </div>
                <!-- End of card 4 -->
            </div>
        <!-- </div> -->
    </section>
</template>


<script>
export default {

    data(){
        return {
          
        }
    },
    methods:{
        moveCard(n){
            document.querySelectorAll('.card').forEach(card => {
                card.style.transform = "rotateY(0deg)";
            });
            const width = window.innerWidth;
            const translateDistance = width * -n;
            document.querySelector('.cards-wrapper').style.transform = `translateX(${translateDistance}px)`;
            document.querySelectorAll('.card').forEach(card => {
                setTimeout(()=>{
                    card.style.transform = "rotateY(-20deg)";
                },1000)
            });
        },
    }
}
</script>

<style lang="scss" scoped>
    .skill-set-page{
        position: relative;
        // margin-top:1000px;
        width:100%;
        height:100%;
        // display: flex;
        background-color: white;
        overflow-x: hidden;
        overflow-y: scroll;
        // border: rgb(136, 255, 0) solid thin;
        // padding: 1.4rem;
        // @include column-horizontal-center();

    
        h1{
            width:100%;
            font-weight: 100;
            color:black;
            font-family: 'Courier New', Courier, monospace;
            font-size:1.4rem;
            padding: 1.4rem 0 0 1.4rem;
            letter-spacing: .1rem;
            // border: blue solid thin;
            @media (min-width:1306px){
                font-size: 2.1rem;
            }
        }

        h3{
            font-weight: 100;
            width:100%;
            color:black;
            font-family: 'Courier New', Courier, monospace;
            font-size:.5rem;
            letter-spacing: .1rem;
            padding: 0 0 0 1.4rem;
            @media (min-width:1306px){
                font-size: 0.9rem;
                margin-bottom:100px;
            }
        }

        .card-switcher{
            width:100%;
            display: flex;
            justify-content: space-between;
            padding-left: 1.4rem;
            padding-right: 1.4rem;
            margin-top:1rem;
            margin-bottom:20px;

            @media (min-width:1306px){
                display: none;
            }

            @media (min-height:768px){
                margin-bottom:40px;
            }
            @media (min-height:1024px){
                margin-bottom:150px;
            }

            button{
                border:none;
                background-color: none;
            }


        }


        .cards-wrapper{      
            width: calc(100vw * 4);
            height: calc(100vh - 125px) ;
            min-height: 400px;
            max-height: 600px;
            padding-bottom:20px;
            display: flex;
            justify-content: left;
            transition: transform 1s;
            // border:red thin solid;
            @media (min-width:1306px){
                transform: translateX(0)  !important;;
                width: 100%;
                justify-content: space-around;
            }
        }

        $width:80vw;
        .card-wrapper{
            width:$width;
            height:100%;
            max-width: 330px;
            max-height: 600px;
            transform-style: preserve-3d; 
            perspective: 100rem;
            margin-right:calc((100vw - $width));
            .card:nth-child(1){
                margin-left:calc((100vw - $width)/1.5);
            }

            @media (min-width:331px){
                // background-color: blue;
                $width:330px;
                width:$width;
                margin-right:calc((100vw - $width));
                .card:nth-child(1){
                    margin-left:calc((100vw - $width)/2);
                }
            }

            @media (min-width:1306px){
                // background-color: blue;
                .card:nth-child(1){
                    margin-left:unset;
                }
                margin-right:unset;
            }

    

  
      

            .card{
                width: 100%;
                height: 100%;
                border: thin solid rgba(238, 235, 235, .5);
                border-radius: 1rem;
                box-shadow: 2rem 1.5rem .8rem #4442424f;
                transform:rotateY(0deg);
                background-color: #ffffff;
                transform-origin: center;
                @include column-horizontal-center(); 

                @media (min-width:1306px){
                    transform: rotateY(-8deg);
                }

            

  


                .card-title{
                    // width: 21rem;
                    // height: 7rem;
                    margin:3rem;
                    @include column-horizontal-center(); 
                    // justify-content: flex-start;
                    
                    
                    h3{
                        width:100%;
                        margin:0;
                        height:50%;
                        font-size: 1.4rem;
                        font-family: $quaternary-font;
                        font-weight: 600;
                        letter-spacing: 0.3rem;
                        text-align: center;
                        padding:0;
                    }
                    h4{
                        // @extend h3;
                        margin-top:.1rem;
                        width:100%;
                        height:50%;
                        font-size: 1.2rem;
                        font-weight:100;
                        letter-spacing: 0.3rem;
                        color: $grey;
                        text-align: center;
                        padding:0;
                    }
                }

                .card-tech-chart{
                    width:100%;
                    height: calc(100% - 7rem);
                    // border:thin solid red;
                    overflow: hidden;
                    @include column-horizontal-center(); 
                    gap:5%;
                    // justify-content:start;
                    padding: 0rem 10px 10px 10px;

                    .tech-wrapper{
                        width:80%;
                        // border:thin solid blue;
                        @include row-horizontal-center(); 
                    
                    
                        .left-side{   
                            // border:thin solid orange;
                            height: 100%;
                            width:2rem;
                            text-align: center;

                            .tech-icon{
                                width:80%;
                                object-fit: cover;
                            }
                        }
                        .right-side{
                            // border:thin solid red;
                            width:100%;
                            height:100%;
                            padding-left: 1rem;
                            
                            .tech-name{
                                // border:thin solid orange;
                                // height:50%;
                                width:100%;
                                font-family: $tertiary-font;
                                font-size:.7rem;
                                color: $grey;
                                letter-spacing: .2rem;
                            }
                            .tech-bar-wrapper{
                                // border:thin solid orange;
                                width:100%;
                                height:50%;
                                position: relative;
                                
                                .bar{
                                    @include vertical-center(); 
                                    width:100%;
                                    height:1px;
                                    background-color: rgb(0, 0, 0);
                                }
                            }
                        }

                    }
                }
            }
        }
    }

    #html-bar{
        width:100%;
    }
    #css-bar{
        width:100%;
    }
    #javascript-bar{
        width:100%;
    }
    #vuejs-bar{
        width:100%;
    }
    #reactjs-bar{
        width:40%;
    }
    #python-bar{
        width:100%;
    }
    #django-bar{
        width:100%;
    }
    #nodejs-bar{
        width:90%;
    }
    #expressjs-bar{
        width:90%;
    }
    #php-bar{
        width:40%;
    }
    #laravel-bar{
        width:20%;
    }
    #mysql-bar{
        width:70%;
    }
    #mongodb-bar{
        width:70%;
    }
    #solidity-bar{
        width:40%;
    }
    #indesign-bar{
        width:100%;
    }
    #xd-bar{
        width:90%;
    }
    #illustrator-bar{
        width:90%;
    }
    #photoshop-bar{
        width:70%;
    }

    

</style>