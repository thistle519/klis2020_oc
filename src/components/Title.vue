<template>
    <div class="view">
        <canvas id="granim-canvas"></canvas>
        <div class="body">

            <div class="hyoushi">
                <img alt="klis oppencampus 2020 logo" class="b-logo d-inline-block align-top"
                    src="../assets/utlogo.svg">
                <!-- <button class="hp-l" src="">学類ホームページ</button> -->
            </div>
            <div class="typer">
                <vue-typer :text='["KLIS OPEN CAMPUS ONLINE 2020","2020.8.30 ONAIR"]' :repeat='0' :shuffle='false'
                    initial-action='typing' :pre-type-delay='70' :type-delay='100' :pre-erase-delay='2000'
                    :erase-delay='150' erase-style='clear' :erase-on-complete='false' caret-animation='blink'>
                </vue-typer>
            </div>

           
            <div class="schedule">
                <iframe style="margin-left:20px;" min-width="300px" src="https://www.youtube.com/embed/vq6n-UlyBAI?controls=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>                
                <!-- <h3>Movie Contents</h3>
                <ul style="list-style: none;">
                    <li>学類プロモーションビデオ</li> 
                    <li>ビブリオバトル説明</li>
                    <li>模擬講義</li>
                    <li>学生へのインタビュー</li>
                    <li>キャンパスツアー</li>
                </ul> -->
                <h3>Live Session</h3>
                <ul style="list-style: none;">
                    <li>スチューデントトーク放送中！</li>
                    <li>10:00~ / 13:00~</li> 
                </ul>
                <h3>学生相談</h3>
                <ul style="list-style: none;">
                    <li>学生相談</li>
                    <li>当日も受け付け中！予約ボタンから今すぐ相談。</li>
                </ul>

                <p style="color:pink; font-weight:bold;">コンテンツ制作 & 更新中！</p>
            </div>
        </div>
    </div>
</template>

<script>
    import Granim from 'granim'

    export default {
        name: 'granim',
        data() {
            return {
                GObj: Object
            }
        },
        mounted() {
            this.GObj = new Granim({
                element: '#granim-canvas',
                name: 'granim',
                opacity: [1, 1],
                states: {
                    'default-state': {
                        gradients: [
                            ['#29323c', '#485577'],
                             ['#ffd700', '#20b2aa'],
                            ['#FF6B6B', '#556270'],
                            ['#483d8b', '#7fffd4']
                        ],
                        transitionSpeed: 7000
                    }
                }
            })
        }
    }
</script>


<style lang="scss" scoped>

        .body {
            z-index: 10;
            display: block;
            position: relative;
            height: 110vh!important;
        }

        #granim-canvas {
            width: 100%;
            height: 110%;
            z-index: 0;
            position: absolute;
            display: block;
            // width: 80vw;
            margin:0 auto;
        }
        .schedule{
            color:whitesmoke;
            margin: 3em 0 0 0;
            padding:0 25vw 0 0;
            text-align:right;
            border-radius: 20px;
            font-size: 90%;
            filter: drop-shadow(0 0 0.1rem black);

        }

        .hyoushi {
            display: block;
            /* text-align: left; */
            margin: 0 2vw;
        }

        .hp-l{
            position: fixed;
            top:0px;
            right: 0px;
            background: rgba($color: #fff, $alpha: .3);
            color: white;
            border-style: none;
             outline:0;
             font-size: 11pt;
             padding:0 10px;
            }
        .hp-l:hover{
            background: rgba($color: #fff, $alpha: .8);
            transition: 0.3s;
            color: rgb(36, 163, 172);
        }

        .b-logo {
            max-width: 370px;
            margin-top: 1vh;
            display: block;
            filter: drop-shadow(0 3px 0.5rem black);
            
        }

        /* TYPER */
        .typer {
            margin: 5% 23vw 0 23vw;
            max-width: 340px;
            padding: 3em 5vw; 
            display: block;
            /* text-align: left; */
            background-color: rgba(255, 255, 255, 0.61);
            border-radius:64% 36% 20% 80% / 38% 31% 69% 62%;

            /* border-radius: 20px; */
        }

        .view {
            height: 110vh;
            margin-bottom: 0 !important;
            padding-bottm: 10vh !important;
        }
</style>
