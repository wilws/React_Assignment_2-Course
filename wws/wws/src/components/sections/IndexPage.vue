<template>
    <section class="index-page" id="index">


        <div class="img-wrapper">
            <div class="name">
                <h1>WAISHUN</h1>
                <h1>WONG</h1>
            </div>
            <div class="img">
                <img :src="require('@/assets/img/font_page/portfile.jpg')">
            </div>
        </div>

        <div class="introduction-wrapper">
            <div class="introduction">
                I am Wai Shun WONG, a self-taught full stack web developer. 
                <br><br>I specialise in VueJs, HTML and CSS/SACS/SCSS to construct frontend web application. For the backend side, I am proficient in using Python + Django or NodeJs + Express framework. I can construct RESTful API for the communication of both front and back ends. I also have knowledge to connect application to MySQL / MongoDB  to preform CRUD.
                <br><br>“Learn” and “Create” are what I passionate about. From design to coding and even to investment, applying newly absorbed knowledge to solve the problem encountered in reality brings me a great satisfaction. 
                <br><br>After Obtaining a Bachelor Degree in Biology in Hong Kong, I pursued a Postgraduate Diploma in Investment Management and Financial Intelligence. The knowledge obtained from postgraduate diploma always stimulating me what programming can do in financial aspect.  I recently finished a course of Solidity and Ethereum. I am seeking chances to participate in a relative project. But, I will never confine myself in single area as life is a journey of learning. My passion for learning and coding drive me to try and challenge as much as I can, no matter it is a frontend project, backend project or others.
          </div>
        </div>



        <!-- <div class="contact">
            <p>github : https://github.com/wilws</p>
            <p>email : wilson.ws.pro@gmail.com</p>
        </div> -->
    </section>
</template>

<script>
export default {
    setup() {
        
    },
}
</script>

<style lang="scss" scoped>

// default size: iPhone 5 : 320px x 568px 

.index-page{
    position:relative;
    width:100%;
    height:100%;
    min-height:568px;
    min-width:320px;
    background-color: rgb(255, 255, 255);
    // border:red thin solid;
    // background-color: red;

    // Rotated Tablet or Desktop
    @media (min-width : 1024px) and (max-height: 1025px){
        display:flex;
        flex-direction: row-reverse;
    }


    $img-wrapper-height: 45%;
    $img-wrapper-min-height: 300px;
    .img-wrapper{
        position: relative;
        height:$img-wrapper-height;
        min-height:$img-wrapper-min-height;
        width:100%;

        // Tablet - Width
        @media (min-width:768px) {
            height:54%;
            min-height:550px;
        }

        // Phone - Height
        @media (min-height:375px){
            min-height:140px;
        }

    

        // Phone - Height
        @media (min-height:414px){
            min-height:220px;
        }




        // Rotated Tablet or Desktop
        @media (min-width : 1024px) and (max-height: 1024px){
            width:100%;
            height:100%;
        }





        .img{
            position: absolute;
            top:0;
            right:0;
            width:80%;
            overflow: hidden;
            height:100%;
            // background-color: green;

            // Rotated Tablet or Desktop
            @media (min-width : 1024px) and (max-height: 1024px){
                width:100%;
                height:100%;
            }

            img{
                position: absolute;
                right:0;
                width: 100%;
                height:100%;
                max-width:340px;
                object-fit:cover;
                overflow: hidden;

                @media (min-width:768px) {
                    max-width:600px;
                }

                @media (min-width : 1024px) and (max-height: 1024px){
                    max-width: unset;
                }
            }
        }



        .name{
            position:absolute;
            bottom:-8%;
            right:30%;
            font-family: 'Noto Sans TC', sans-serif;
            font-size: 1.5rem;
            letter-spacing: 0.3rem;
            line-height: 1.8rem;
            text-align: right;
            z-index: 1;
            padding: 0rem;
            background-color: rgba(256,256,256,0.5);

            // Phone - Width
            @media (min-width: 375px) {
                font-size: 1.9rem;
                letter-spacing: 0.3rem;
                line-height: 2.5rem;
                bottom:-3%;
            }

            // Tablet - Width
            @media (min-width:768px) {
                font-size: 3.9rem;
                letter-spacing: 0.3rem;
                line-height: 5.14rem; 
                bottom:-7%;
            }

            // Tablet - Height
            @media (min-height:1180px) {        
                 bottom: -6%;
            }

            @media (min-width : 1024px) and (max-height: 1024px){
                font-size: 2.7rem;
                letter-spacing: 0.3rem;
                line-height: 3.44rem;
                top: 0.7%;
                right: 87.1%;
                background-color: transparent;
                height:0;
            }

            @media (min-width : 1360px) and (max-height: 1360px){
                font-size: 3.5rem;
                letter-spacing: 0.5rem;
                line-height: 4.84rem;
            }


             @media (min-width : 1360px) and (max-height: 1360px){
                right: 91.5%;
            }


            h1:nth-child(2){
                margin-top:.2rem;
            }

        }

        
    }

    .introduction-wrapper{
        position: relative;     
        height: calc(100% - 320px - 4%);
        width: 100%;
        padding:0 2.3rem 0 2.3rem;
        margin:10% 0 1px 0;
        overflow: scroll;
        z-index: 0;

        // background-color: blue;;


        // Phone - Width
        @media (min-width: 375px){
            height: calc(100% - 375px - 4%);
            margin:5% 0 1px 0;
        }

        // Tablet - Width
        @media (min-width: 820px){
            padding:0 5rem 0 5rem;
        }

        // Phone - Height
        @media (min-height:667px){
            height: calc(100% - 360px);
            margin: 9% 0 1px 0;
        }

        @media (min-height:720px){
            height: calc(100% - 381px);
        }

        @media (min-height:812px) {        
            height: calc(100% - 425px);      
            margin: 6% 0 1px 0;
        }

        @media (min-height:896px) {        
            height: calc(100% - 500px);      
            margin: 6% 0 1px 0;
        }

        // Tablet - Height
        @media (min-height:1024px){
            height: calc(100% - 730px);
            padding:0 5rem 0 5rem;
            margin: 9% 0 1px 0;
        }

        // Tablet - Height
        @media (min-height:1366px){
            height: calc(100% - 900px);
            padding:0 5rem 0 5rem;
            margin: 9% 0 1px 0;
        }


        @media (min-width : 1024px) and (max-height: 1024px){
            height:100%;
            margin: 0% 0 1px 0;
            padding-top:15%;
   
        }




        .introduction{
            position: relative;

            // background-color: rgb(0, 255, 0);;
   
            width:100%;
            height:auto;
            font-family: $primary-font;
            color: black ;
            font-size: 0.6rem;
            letter-spacing: 0rem;
            line-height: 1.2rem;
            text-align: justify;
            // border:thin red solid;




            // Tablet Width
            @media (min-width:820px){
                font-size: 1.2rem;
                letter-spacing: 0.1rem;
                line-height: 2.2rem;
            }

            @media (min-height:720px){
                font-size: 0.8rem;
                letter-spacing: 0rem;
                line-height: 1.4rem;
            }


            @media (min-height:814px){
                font-size: 0.8rem;
                letter-spacing: 0rem;
                line-height: 1.1rem;
            }

            // Tablet Height
            @media (min-height:1024px){
                font-size: 1.1rem;
                letter-spacing: 0.1rem;
                line-height: 1.6rem;
            }

            @media (min-height:1366px){
                font-size: 1.6rem;
                letter-spacing: 0.1rem;
                line-height: 2.2rem;
            }


            @media (min-width : 1024px) and (max-height: 1024px){
                font-size: 0.8rem;
                letter-spacing: 0rem;
                line-height: 1.5rem;
            }

             @media (min-width : 1360px) and (max-height: 1360px){
                font-size: 1.1rem;
                letter-spacing: 0rem;
                line-height: 2.2rem;
            }
        }


    }



    .contact{
        position:absolute;
        right:5rem;
        bottom:5rem;
        color: rgb(141, 139, 139);
        font-family: $secondary-font;
        font-size: 1.4rem;
        letter-spacing: 0.3rem;
        text-align: right;

    }
}


</style>