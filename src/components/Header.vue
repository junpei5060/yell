<template>
    <div>
        <h1 class="ServiceName">
        Delivery Yell
        <p class="introduceService">〜誰かのエールで夢を叶えよう〜</p>
        </h1>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Sacramento');

div{
    width: 1080px;
    margin: 0 auto;
}
    
.ServiceName{
    font-size: 60px;
    text-align: center;
    margin: 32px;
    padding-bottom: 0;
    border-bottom: solid 3px #ffc778;
    position: relative;
    font-family: 'Sacramento', cursive;
    margin: 0;
}

.ServiceName:after {
    position: absolute;
    content: " ";
    display: block;
    border-bottom: solid 3px skyblue;
    bottom: -3px;
    width: 50%;
}

.introduceService{
    font-size: 16px;
    padding-top: 1px;
    margin: 3px auto;
}
</style>