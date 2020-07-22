<template>
    <div class="row">
        <div class="col-md-12 text-center">
            <h1 class="mt-5 pt-5">LOVE DAYS</h1>
            <div id="clock-box">
                    <div id="clock">
                        <date>0 DAYS</date>
                        <time>00:00:00</time>
                    </div>
                </div>
                
                <div id="info">
                    <div class="one">
                            <img src="img/main.jpg" class="avt">
                            <p>Lu minh thong</p>
                    </div>
                    <div id="heart">
                            <!-- ❤<anni>...</anni> -->
                    </div>
                    <div class="two">
                            <img src="img/main.jpg" class="avt">
                            <p>Lu minh thong</p>
                    </div>
                </div>
                
                <div id="music">
                    <audio loop autoplay controls>Your browser does not support the audio element.</audio>
                </div>
                <footer>Thank you for your love 💕</footer>
            </div>
        </div>
</template>

<script>
export default {
    data() {
        return {
            counter: 0,
        }
    },
    methods: {
        helloWord() {
            this.couter = 4
        }
    }
}
</script>