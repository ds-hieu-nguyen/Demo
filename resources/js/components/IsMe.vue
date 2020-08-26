<template>
<div>
    <div class="row">
        <div class="col-md-12 text-center  img-background">
            <h1 class="mt-5 pt-5"></h1>
            <div id="clock-box">
                <div id="clock">
                    <date>{{time}} DAYS</date>
                    <time>{{currTime.getHours()}}:{{currTime.getMinutes()}}:{{currTime.getSeconds()}}</time>
                </div>
            </div>
                
            <div id="info">
                <div class="one">
                        <img src="aimg/Love.jpg" class="avt">
                        <p>A</p>
                </div>
                <div id="heart">
                        ❤<anni>...</anni> 
                </div>
                <div class="two">
                        <img src="aimg/Loveyou.jpg" class="avt">
                        <p>b</p>
                </div>
            </div>
                
            <div id="music">
                <vue-audio file="myLocalFile"></vue-audio>
                <audio loop autoplay src="mp3/a123.mp3" controls="controls"></audio>
            </div>
            <hr>
        </div>
    </div>
    <div class="row">
        <div class="col-md-3 offset-md-5">
            <h1><strong>My</strong></h1>
            <div class="composition">
                <img src="img/1.jpg" alt="photo1"
                    class="composition__photo composition__photo--p1">
                <img src="img/2.jpg" alt="photo2"
                    class="composition__photo composition__photo--p2">
                <img src="img/3.jpg" alt="photo3"
                    class="composition__photo composition__photo--p3">
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            time: 0,
            message: 'Current Time:',
            currTime: new Date(),
        }
    },
   
    created() {
        this.startName();
        setInterval(()=>{
				this.currTime = new Date();
			},1000)
    },
    
    computed: {
        sec() {
            return this.currTime.getSeconds()*6;
        },
        min() {
            return this.currTime.getMinutes()*6 + this.currTime.getSeconds()/10 ;
        },
        hour() {
            return this. currTime.getHours()*30 + this.currTime.getMinutes()/2;
        }
    },

    mounted() {
    },
    methods: {
        startName() {
            var time1 = new Date();
            console.log(time1);

            var time2 = new Date('2019-07-21');
            console.log(time2);

            var t1 = time1.getTime();
            var t2 = time2.getTime();

            this.time = parseInt((t1-t2)/(24*3600*1000));
        },
        
    }
}
</script>