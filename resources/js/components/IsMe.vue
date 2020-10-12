<template>
<div>
    <div class="row">
        <div class="col-md-12 text-center  img-background">
            <h1 class="mt-5 pt-5"></h1>
            <div id="clock-box">
                <div id="clock" class="text-danger">
                    <date>{{time}} DAYS</date>
                    <time>{{currTime.getHours()}}:{{currTime.getMinutes()}}:{{currTime.getSeconds()}}</time>
                </div>
            </div>
                
            <div id="info">
                <div class="one">
                        <img src="img/Love.jpg" class="avt">
                        <p>A</p>
                </div>
                <div id="heart">
                        ❤<anni>...</anni> 
                </div>
                <div class="two">
                        <img src="img/Loveyou.jpg" class="avt">
                        <p>b</p>
                </div>
            </div>
                
            <div id="music">
                <vue-audio file="myLocalFile"></vue-audio>
                <audio loop autoplay src="mp3/a2.mp3" controls="controls"></audio>
            </div>
            <hr>
        </div>
    </div>
    <div class="row mt-5">
        <div class="col-md-12 text-center">
            <h1 class="mb-5"><strong>Ảnh đây nè !!!</strong></h1>
        </div>
    </div>
    <div class="row mt-5">
        <div class="col-md-3 offset-md-5">
            <div class="composition mt-5">
                <img src="img/1.jpg" alt="photo1"
                    class="composition__photo composition__photo--p1">
                <img src="img/2.jpg" alt="photo2"
                    class="composition__photo composition__photo--p2">
                <img src="img/3.jpg" alt="photo3"
                    class="composition__photo composition__photo--p3">
            </div>
        </div>
    </div>
    <footer class="page-footer font-small mdb-color darken-3 pt-4 bg-info">

        <!-- Footer Elements -->
        <div class="container">
            <div class="row d-flex justify-content-center">
                <div class="col-md-6">
                    <div class="embed-responsive embed-responsive-16by9 mb-4">
                        <iframe width="560" height="315" src="https://www.youtube.com/embed/7hN2EhL7Jg0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-copyright text-center text-danger py-3 off-me" >Cô Bé Của Anh:
            <a href="https://www.facebook.com/minhhieu97.hust/">Hiu</a>💕
            <a href="https://www.facebook.com/Hang.ntt2001/">Han</a>
        </div>
</footer>
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