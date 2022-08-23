<template>
    <section class="assignment" id="assignment">
        <h1>Assignment</h1>

        <p>Udemy is my source of knowledge. 
            <br>During the learning process, I follow the videos to complete the assignments,Whenever I encounter something that I don`t understand , I will click “Pause” on the video to search for the  reason rather than clicking “Next” to let it remains mysterious. I understand every single lines that I type in my assignment.  And therefore I can replicate every effect / output of the assignment. 
            <br>It is meaningless to fake what you know as time will reveal it anyway.
        </p>
        <div class="web-assignments">
            <h2>HTML / CSS / JS</h2>
            <div class="assignments-wrapper">
                <a href="https://wilws.github.io/Responsive_Assignment_1-Foods/" target="_blank"><img :src="require('@/assets/img/final_page/assignment1.png')"></a>
                <a href="https://wilws.github.io/Responsive_Assignment_3-Agent/" target="_blank"><img :src="require('@/assets/img/final_page/assignment2.png')"></a>
                <a href="https://wilws.github.io/Responsive_Assignment_4-Apple/" target="_blank"><img :src="require('@/assets/img/final_page/assignment3.png')"></a>
                <a href="https://wilws.github.io/Responsive_Assignment_6-Car/" target="_blank"><img :src="require('@/assets/img/final_page/assignment4.png')"></a>
                <a href="https://wilws.github.io/Responsive_Assignment_9-Wine/" target="_blank"><img :src="require('@/assets/img/final_page/assignment5.png')"></a>
                <a href="https://wilws.github.io/Responsive_assignment_8-Road/" target="_blank"><img :src="require('@/assets/img/final_page/assignment7.png')"></a>
                <a href="https://wilws.github.io/Responsive_Assignment_7-Architect/" target="_blank"><img :src="require('@/assets/img/final_page/assignment8.png')"></a>
                <a></a>
            </div>
        </div>
        <div class="other-assignment">
            <h2>ETHEREUM AND SOLIDITY</h2>
            <a href="https://www.udemy.com/certificate/UC-2049b1c9-815d-4d10-9524-507fb4282408/" target="_blank"> >>> My Udemy Certificate  </a><br>
            <a href="https://github.com/wilws/solidity_assignment_1-inbox.git" target="_blank">https://github.com/wilws/solidity_assignment_1-inbox.git</a><br>
            <a href="https://github.com/wilws/solidity_assignment_2-lottery_react.git" target="_blank">https://github.com/wilws/solidity_assignment_2-lottery_react.git</a><br>
            <a href="https://github.com/wilws/solidity_assignment_3-kickstart.git" target="_blank">https://github.com/wilws/solidity_assignment_3-kickstart.git</a>
        </div>

        <div class="left-cover">                                  
            <img :src="require('@/assets/img/final_page/cover.jpg')" class="dog-img">
            <div class="my-dog-tag">
                <div class="arrow-wrapper">
                    <div class="left-line"></div>
                    <div class="middle-line"></div>
                    <div class="right-line"></div>
                </div>
                <p>My Dog</p>
            </div>
        </div>
    </section>
</template>


<script>
export default {
    setup() {
        
    },
}
</script>

<style lang="scss" scoped>

.assignment{
    position: relative;
    width:100%;
    height:100%;
    padding: 4rem;
    background-color: black;
    color:white;
    display: flex;
    flex-direction: column;
    justify-content: space-between;


    h1{
        width:100%;
        font-family: $secondary-font;
        font-size:3rem;
        letter-spacing: .1rem;
        text-align: left;
        // border:red solid thin;
    }
    p{
        position: relative;
        margin-top:2rem;
        width:60%;
        font-family: $secondary-font;
        // border:green solid thin;
        font-size:2.4rem;
        letter-spacing: .1rem;
        z-index: 10;

    }
    .web-assignments{
        position: relative;
        z-index: 2;
        margin-top:10rem;
        // border:yellow solid thin;
        width:65rem;
        height:27rem;

        h2{
            margin-bottom:1rem;
            font-family: 'Roboto', sans-serif;
            font-weight: 300;
            font-size:3.1rem;
            letter-spacing: .4rem;
        }
        
        .assignments-wrapper{
            width:100%;
            height: 100%;
            // border:blue solid thin;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            
            
            a {
                width:15rem;
                height:7rem;
                img{
                    width:100%;
                }
            }
        }
    }
    .other-assignment{
        // border:red solid thin;
        position: relative;
        margin-top:8rem;
        width:120rem;
        z-index: 10;

        h2{
            font-family: 'Roboto', sans-serif;
            font-weight: 300;
            font-size:3.1rem;
            margin-bottom:1rem;
            letter-spacing: .4rem;

        }
        a{
            font-size: 2rem;
            font-family: 'Courier New';
            color: white;

        }
        p{
            margin:0;
            font-size: 1.5rem;
            font-family: 'Courier New';
            width:100%;
            a{
                font-size: 1.5rem;
                letter-spacing: .2rem;
            }
        }
       
    }

    .left-cover{
        position: absolute;
        // border:orange solid thin;
        height:100rem;
        right:20rem;
        top:0rem;
        z-index: 1;

        .dog-img{
            height:100%;
        }
        .my-dog-tag{
            // border:rgb(124, 63, 63) solid thin;
                position:absolute;
                width:10rem;
                height:10rem;
                top:23%;
                right:18%;
                z-index: 11;
            .arrow-wrapper{
                // border:grey solid thin;
                position:absolute;
                width:70%;
                height:70%;
                left:0rem;
                top:1%;
                transform:rotateZ(48deg);
    
                .left-line{
                    position:absolute;
                    top:42%;
                    background-color:white;
                    width:2rem;
                    height:.1rem;
                    transform:rotateZ(-30deg);
                    border-radius: 5px;
                }
                .middle-line{
                    position:absolute;
                    top:50%;
                    left:.2rem;
                    background-color:white;
                    width:5rem;
                    height:.1rem;
                    border-radius: 5px;
                }
                .right-line{
                    position:absolute;
                    top:57%;
                    background-color:white;
                    width:2rem;
                    height:.1rem;
                    transform:rotateZ(30deg);
                    border-radius: 5px;
                }
            }
            p{
                position:absolute;
                bottom:20%;
                left:20%;
                color:white;
                width:100%;
                font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            }
        }
    }
}

</style>