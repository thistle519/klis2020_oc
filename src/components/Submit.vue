<template>
  <div>
    <button class="sbutton" type="button" @click="open"><img class="sbimg" src="../assets/submitbutton.png"></button>
    <modal name="submit">
      <div class="bm">
        <div class="bmcon">
        <h1 class="title white shadow">Zoom学生相談<br>事前登録</h1>
        <h4 style="margin:1em 0; color:paleturquoise" class="lightcoral">8月30日開催</h4>
        <p class="white shadow">Zoomによるオンライン学生相談を行います。聞きたいこと，相談したいことがある方はぜひお申し込みください！</p>
        <div class="yoyaku"><a href="#cal">オンライン相談<br>今すぐ予約！</a></div>
        
        <img style="margin-top:3em;" class="shadow" alt="zoom logo" width="70px" src="../assets/zoom_icon.png">
        <br>
        <a href="https://apps.apple.com/jp/app/zoom-cloud-meetings/id546505307"><img  alt="appstore" height="40px" src="../assets/appstore.svg"></a>
        <a href="https://play.google.com/store/apps/details?id=us.zoom.videomeetings&hl=ja"><img  style="filter:grayscale(1);" alt="google play" height="60px" src="../assets/play.png"></a>

        <h4 id="cal" style="margin-top:2em;" class="shadow white">予約</h4>
        <p class="shadow white">予約カレンダー or<a target="_blank" rel=”noopener” href="https://coubic.com/klis2020"> こちら</a>からいますぐ簡単予約！</p>
        <p class="shadow white" style="font-size:5pt;">*Microsoft InternetExploerには非対応。Chrome/Edge等をお使いください。利用は無料，通信料等がかかる場合があります。</p>
        <iframe class="glass" src="https://coubic.com/klis2020/widget/calendar?from_pc=listMonth&from_sp=listMonth" style="border: none; width: 100%; height: 780px;" allowtransparency='true' frameborder=0 scrolling="no"></iframe>
        </div>
        <button class="cb button" type="button" @click="close">×</button>
      </div>
    </modal>
  </div>
</template>

<script>
export default {
  methods: {
    open () {
      this.$modal.push('submit')
    },

    close () {
      this.$modal.pop()
    }
  }
}
</script>

<style scoped>
.yoyaku{
    background: darkturquoise;
    border-radius: 10px;
    border:solid 2px whitesmoke;
    width: 200px;
    font-weight: 400;
    text-align:center;
    margin:2em auto 0 auto;
}
.yoyaku a{
  color:whitesmoke!important;
  text-decoration: none;
}
.yoyaku:hover{
    background:cyan;
    transition: 80ms;
}

.bmcon{
    margin-top:4em!important;
    z-index: 11;
    position: relative;
    display: block;
    top:0px;
    margin: 1vh 1vw;
    text-align: center;
}
.shadow{
    filter: drop-shadow(0 0 0.75rem black);
}
.white{
    color: whitesmoke;
}
.bm{
    width: 100%;
    height: 100%;
    position: absolute;
    display: block;
    top:0px;
    z-index: 10;
    /* background: rgba(22,22,22, 0.5); */
    background-color: rgba(0,0,0, 0.6);
    backdrop-filter: blur(6px);
    /* background-image: url("https://www.transparenttextures.com/patterns/diagmonds-light.png"); */
    /* This is mostly intended for prototyping; please download the pattern and re-host for production environments. Thank you! */
    padding: 10vh 5vw;
    overflow: auto;
    transition: 80ms;
}
.cb{
    border-style: none;
    background: rgba(255,255,255, 0.8);
    padding: 18px 25px;
    border-radius:50%;
    outline:0;
    position:absolute;
    z-index: 100;
}
.cb:hover{
    transition: 0.5s;
    background: black;
    color: whitesmoke!important;
}

.button{
    z-index: 0;
    position: fixed;
    top:2vh;
    right: 30px;
}

.sbutton{
    position: fixed;
    bottom: 90px; 
    right: 5px;  
    border-style: none;
    background:rgba(0,0,0,0);
    z-index: 10;
    outline:0;
}

.sbutton:hover{
  filter: contrast(200%);
  transition: 80ms;
}

.sbimg{
  height: 130px;
  min-height: 10vh!important;
}

.glass{
  filter: contrast(170%);
}


</style>

