<template>
    <div class="card" :style="{width:width + 'px', height:height + 'px'}">
        <header class="card_thumb">
            <a href="#">
                <img :src="imgSrc">
            </a>
        </header>
        <div class="card_body">
            <h2 calss="card_title">{{title}}</h2>
            <div class="card_subtitle">{{subtitle}}</div>
            <p class="card_desc">
                {{desc}}
            </p>
        </div>
        <footer class="card_footer">
           <a :href="footer_link">{{footer_text}}</a> 
        </footer>
    </div>
</template>

<script>
export default {
    name: 'card',
    props:{
        width: {
            type: Number,
            default: 370
        },
        height:{
            type: Number,
            default: 430
        },
        imgSrc: {
            type: String,
            default: 'https://hbimg.huabanimg.com/1ccac3a5bdc74168e8b91d886a12be75471e82ce40b19-MoLdbk_fw658'
        },
        title:{
            type: String,
            default: '越努力，越幸运!' 
        },
         subtitle:{
            type: String,
            default: 'QHMILK' 
        },
        desc:{
            type: String,
            default: '正文的详细内容描述,越努力，越幸运,机不可失，失不再来。正文的详细内容描述,越努力，越幸运,机不可失，失不再来'
        },
        footer_text:{
            type: String,
            default: '想要知道更多...'
        },
        footer_link:{
            type:String,
            default: '#'
        }
    }
}
</script>

<style scoped>
.card{
    width: 370px;
    height: 420px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translateX(-50%) translateY(-50%) translateZ(0);
    box-sizing: border-box;
    background: #eee;
    box-shadow: 0 0 20 rgba(0,0,0,0.1);
    overflow: hidden;
    transition: box-shadow 0.5s;
}

.card a{
    color: inherit;
    text-decoration: none;
}

.card:hover{
    box-shadow: 0 0 50px rgba(0,0,0,0.3);
}

.card_thumb{
    height: 245px;
    overflow: hidden;
    background: #000;
    transition: height 0.5s;
}

.card_thumb img{
    width: 100%;
    display: block;
    opacity: 1;
    transform: scale(1);
    transition: opacity 0.5s , transform 0.5s;
}

.card:hover .card_thumb{
    height: 130px;
}

.card:hover .card_thumb img{
    opacity: 0.6;
    transform: scale(1.2);
}

.card_body{
    padding:  0 10px;
}

.card_title{
    margin: 0;
    padding: 0;
    color: #000;
    font-size: 22px;
    font-weight: bold;
    text-transform: uppercase;
}

.card_subtitle{
    margin: 0;
    font-size: 19px;
    color: LightSkyBlue;
}

.card_desc{
    color: #666c74;
    line-height: 27px;
    opacity: 0;
    transform: translateY(5px);
    transition: all 0.3s;
    transition-delay: 0s;
    height: 7rem;
    overflow: hidden;
}

.card:hover .card_desc{
    opacity: 1;
    transform: translateY(0);
    transition-delay: 0.2s;
}

.card_footer{
    padding: 0 10px 22px 10px;
    font-size: 11px;
    color: #A3A9A2;
    position: absolute;
    bottom: 0;
}
</style>