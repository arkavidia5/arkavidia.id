<template>
    <v-layout row v-if="direction === 'right'" align-center>
        <v-flex xs5 md5 sm5 justify-end align-center flex text-right>
            <img :src=image alt="" height="100" style="margin-right:-40px"/>
        </v-flex>
        <v-flex xs2 md2 sm2 center>
            <div class="vertical-line"></div> 
            <div class="right-horizontal-line"></div>
            <div class="center-circle"></div>
            <div class="right-ball"></div>
        </v-flex>
        <v-flex class="flex align-center justify-left" xs5 md5 sm5 style="padding-left:20px;">
            <h2 align="left">
                {{title}}
            </h2>    
            <h3 align="left"> 
                {{time}}
            </h3>
            <h4 align="left">
                {{description}}
            </h4>
        </v-flex>
    </v-layout>
    <v-layout row align-center v-else>
        <v-flex class="flex align-center" xs5 md5 sm5 style="padding-right:20px;">
            <h2 align="right">
                {{title}}
            </h2>    
            <h3 align="right">
                {{time}}
            </h3>
            <h4 align="right">
                {{description}}
            </h4>
        </v-flex>
        <v-flex xs2 md2 sm2 center>
            <div class="vertical-line"></div> 
            <div class="left-horizontal-line"></div>
            <div class="center-circle"></div>
            <div class="left-ball"></div>
        </v-flex>
         <v-flex xs5 md5 sm5 text-left>
            <img :src=image alt="" height="100" style="margin-left: -40px"/>
        </v-flex>
    </v-layout>
</template>

<script>
export default {
    name: 'TimelineItem',
    props: ["direction","image","title","time","description"]

}
</script>

<style scoped>
    .row {
        height: 120px;
        color: rgb(0,184,184);
        /* background: white; */
        /* margin:10px; */
    }
    .center {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        width: 100%;
    }
    .center .vertical-line {
        position: absolute;
        background: rgb(95,95,95);
        height: 100%;
        width: 5px;
    }
    .center .center-circle {
        position: absolute;
        height:25px;
        width:25px;
        border: 5px solid rgb(95,95,95);
        border-radius: 50%;
        background: rgb(253,247,0);
    }
    .center .right-horizontal-line{
        height:5px;
        width:45%;
        background: rgb(95,95,95);
        position: absolute;
        left:50%;
    }
    .center .right-ball {
        position: absolute;
        height: 15px;
        width: 15px;
        background: rgb(95,95,95);
        border-radius: 50%;
        left: 95%;
    }
    .center .left-horizontal-line{
        height:5px;
        width:45%;
        background: rgb(95,95,95);
        position: absolute;
        right:50%;
    }
    .center .left-ball {
        position: absolute;
        height: 15px;
        width: 15px;
        background: rgb(95,95,95);
        border-radius: 50%;
        right: 95%;
    }
    .text-right {
        text-align: right;
    }
    .text-left {
        text-align: left;
    }
</style>
