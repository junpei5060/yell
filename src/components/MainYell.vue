<template>
    <div class="main">
        <div id="app">
            <div class="box26">
                <p class="yell" >{{ result }}</p>
            </div>
            <button class="btn-stitch" onclick="disabled = true;" @click="yellrandom">エールをもらう</button>      
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data(){
        return{
            result:"誰かのエールで夢を叶えよう",
            yellResult:[]
        }
    },
    mounted (){
        axios.get(
            "https://zisyuu.microcms.io/api/v1/yell1?depth=2",
            {
            headers:{
                "Content-Type":"application/json",
                "X-API-KEY":"b1112041-04c4-4c90-a8cb-0b08a82d177e"
            },           
            })
            .then(response => {this.yellResult = response.data.contents,
            console.log(this.yellResult)
            })
            .catch(response => console.log(response))
    },
    methods:{
        yellrandom(){
            const num = Math.floor(Math.random()*this.yellResult.length);
            this.result = this.yellResult[num].content;
            console.log(this.result)
        }
    }
}
</script>

<style scoped>
.main{
    width: 1080px;
    margin: 0 auto;
}

.box26 {
    position: relative;
    margin: 2em 0;
    padding: 5em 1em;
    width: 900px;
    margin: 0 auto;
    border: solid 3px #95ccff;
    border-radius: 20px;
    margin-top: 20px;
}
.box26 .box-title {
    position: absolute;
    display: inline-block;
    top: -13px;
    left: 10px;
    padding: 0 9px;
    line-height: 1;
    font-size: 19px;
    background: #FFF;
    color: #95ccff;
    font-weight: bold;
}
.box26 p {
    margin: 0; 
    padding: 0;
}

.yell{
    text-align: center;
    font-size: 16px;
    color: rgb(245, 140, 140);
    font-weight: bold;
    white-space: pre-wrap;
}

.btn-stitch {
    width:119px;
    padding: 0.5em 1em;
    text-decoration: none;
    background: #668ad8;
    color: #FFF;
    border-radius: 10px;
    box-shadow: 0px 0px 0px 5px #668ad8;
    border: dashed 1px #FFF;
    margin-top: 64px;
    margin-left: 342px;
    width: 400px;
    text-align: center;

}

.btn-stitch:hover {
    border: dotted 1px #FFF;
}

</style>