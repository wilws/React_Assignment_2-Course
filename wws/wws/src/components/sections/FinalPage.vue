<template>
    <section class="assignment">
        <h1>Assignment</h1>

        <p>Udemy is my source of knowledge. <br>During the learning process, I follow the videos to complete the assignments.<br>
Whenever I encounter something that I don`t understand , I will click “Pause”<br>on the video to search for the  reason rather than clicking “Next” to let it remains mysterious. I understand every single lines that I type in my assignment.  And therefore I can replicate every effect / output of the assignment. 
<br><br>It is meaningless to fake what you know as time will reveal it anyway.</p>
        <div class="web-assignments">
            <h2>HTML / CSS /JS</h2>
            <div class="assignments-wrapper">
                <a><img :src="require('@/assets/img/final_page/assignment1.png')"></a>
                <a><img :src="require('@/assets/img/final_page/assignment2.png')"></a>
                <a><img :src="require('@/assets/img/final_page/assignment3.png')"></a>
                <a><img :src="require('@/assets/img/final_page/assignment4.png')"></a>
                <a><img :src="require('@/assets/img/final_page/assignment5.png')"></a>
                <a><img :src="require('@/assets/img/final_page/assignment7.png')"></a>
                <a><img :src="require('@/assets/img/final_page/assignment8.png')"></a>
            </div>
        </div>
        <div class="other-assignment">
            <h2>ETHEREUM AND SOLIDITY</h2>
            <p></p>
            <a></a>
            <a></a>
            <a></a>
        </div>
                                             
        <img :src="require('@/assets/img/final_page/cover.jpg')" class="dog-img">
        <div class="arrow-wrapper">
            <div class="left-line"></div>
            <div class="middle-line"></div>
            <div class="right-line"></div>
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
    width:100%;
    height:100%;

    h1{}
    arrow
}

</style>