<template>
    <div>
        <div class="design_center_1">
        <PCHeader :is-dark="true"/>
        <div class="design_center_container">
            <img src="../../assets/images/artwork_1.png" alt="" width="100%" height="1425px">
            <div class="design_center_article">
                <div style="height: 237px;"></div>

                <p class="title">Design<span style="font-weight: 300;">-centred</span></p>
                <p class="description">We’re on a mission to bring companion robots into homes everywhere. We believe that Maah is the perfect blend of form and function, ascting both as a stylish piece of interior design and a beloved pet.
                    <br><br>
                    As a brand, we are ruling for a new aesthetic in opposition to the current state of robotics. Maah is the result of co-creation and participatory design with our communities.</p>
            </div>
        </div>
    </div>
    <div class="design_center_2">
        <p>boundless
        <br>possibilites</p>
    </div>
    <div class="design_center_3">
        <div class="design_center_3_inner_1">
            <div class="design_center_3_desc">
                <img src="../../assets/images/maah_chair_1.png" alt="">
                <p class="title">MOOSKIT</p>
                <p class="description">From the Shetland Islands</p>
            </div>
            <div class="design_center_3_desc">
                <img src="../../assets/images/maah_chair_2.png" alt="">
                <p class="title">SHOLMIT</p>
                <p class="description">From the Shetland Islands</p>
            </div>
            <div class="design_center_3_desc">
                <p class="right_title">
                    THE 
                    <br>HIGHLAND
                    <br>RANGE</p>
                <p class="right_description">Designed, sourced, developed 
                    and manufactured in Scotland, 
                    using natural yarns from the 
                    Shetland Islands.</p>
                <img src="../../assets/images/maah_chair_3.png" alt="">
                <p class="title">EESIT</p>
                <p class="description">From the Shetland Islands</p>
            </div>
            <div class="design_center_3_desc_bottom">
                <p class="subtitle">behind</p>
                <p class="title">THE COLLECTION</p>
                <p class="description">the first collection highlights our ambition to create another model of 
                    development for companion robots. where aesthetics meets sustainability 
                    and craft. Our robots are crafted using cutting-edge textile development 
                    methods, rather than traditional rigid plastic exteriors. This not only elevates
                    the aesthetic of Maah but also allows us to take a more responsible approach
                    to their development. We believe that this new development model will not
                    only improve the positive impact of our technology but also enhance the bond 
                    between you and your companion robot.</p>
            </div>
        </div>
    </div>
    <div style="height: 150px;"></div>
    <div class="design_center_4">
        <video autoplay loop muted webkit-playsinline playsinline width="100%">
            <source src="/videos/maah_video_3.mp4" type="video/mp4">
            Your browser does not support the video tag.
            </video>
        <div class="design_center_4_top">
            a companion
            <br> matching your
            <br> <span style="font-weight: 500;">unique</span> style
        </div>
        <div class="design_center_4_bottom">
            <div>
                <p class="design_center_4_bottom_title" style="text-align: center; padding-bottom: 75px;">Adaptability by 
                    <br> Design</p>
                <p class="design_center_4_bottom_description">Even if turned off, Maah will still live and exist in your personal space. It is designed to fit your tastes and blend in or stand out in your environment. Maah is interior design as a means , not an end</p>
            </div>
            <img src="../../assets/images/maah_chair_4.png" alt="">
        </div>
    </div>

    <div style="height: 100px;"></div>
    <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import PCHeader from '../headers/PCHeader.vue';
export default {
    name: 'PCDesignCenter',
    components: { PCHeader },
    data() {
        return {
            // Your data properties here
        };
    },
    methods: {
        // Your methods here
    },
    // Other lifecycle hooks and component options here
};
</script>

<style scoped>
.design_center_1 {
    background: #FDF9F3;
    width: 100%;
}
.design_center_top {
    display: flex;
    flex-direction: column;
    align-items: center;
}


.design_center_top > img {
    width: 320px;
    padding: 70px 0 85px;
}

.design_center_container {
    position: relative;
}

.design_center_container img {
    padding-left: 20%;
    object-fit: contain;
}

.design_center_article {
    position: absolute;
    top: 150px;
    left: 10%;
}

.design_center_article > .title {
    color: #000;
    font-family: Spartan;
    font-size: 100px;
    font-style: normal;
    font-weight: 700;
    line-height: 90px; /* 90% */
}

.design_center_article > .description {
    margin-top: 110px;
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 200;
    line-height: 37px; /* 148% */
    width: 30%;
}

.design_center_2 {
    position: relative;
    width: 100%;
    height: 1050px;
    background: url(../../assets/images/maahs.png) lightgray 50% / cover no-repeat;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    
}

.design_center_2 p {
    position: absolute;
    top: 50%;
    right: 5%;
    color: #000;
    text-align: right;
    font-family: Melodrama;
    font-size: 90px;
    font-style: normal;
    font-weight: 500;
    line-height: 94px; /* 104.444% */
}

.design_center_3 {
    background: #FFF;
    padding: 150px 0 0 0;

}

.design_center_3_inner_1 {

    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 3vw;
    padding: 0 10% 0 3%;
}

.design_center_3_desc:nth-child(1) {
    grid-column: 1 / 2;
    grid-row: 1 / 3;
}

.design_center_3_desc:nth-child(2) {
    margin-top: 70%;
    grid-column: 2 / 3;
    grid-row: 1 / 3;
}

.design_center_3_desc:nth-child(3) {
    grid-column: 3 / 4;
    grid-row: 1 / 4;
}

.design_center_3_desc_bottom {
    padding-right: 100px;
    grid-column: 1 / 3;
    grid-row: 3 / 4;
}

.design_center_3_desc img {
    width: 100%;
}

.design_center_3_desc > .title {
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 300;
    line-height: 37px; /* 148% */
    margin: 40px 0 10px;
}

.design_center_3_desc > .description {
    color: #000;
    font-family: Spartan;
    font-size: 20px;
    font-style: normal;
    font-weight: 300;
    line-height: 37px; /* 185% */
}

.design_center_3_desc > .right_title {
    color: #000;
    font-family: Spartan;
    font-size: 3vw;
    font-style: normal;
    font-weight: 100;
    line-height: 4vw; /* 122.222% */
    letter-spacing: -7.2px;
}

.design_center_3_desc > .right_description {
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 100;
    line-height: 37px; /* 148% */
    padding: 30px 0 120px 0;
}

.design_center_3_desc_bottom > .subtitle {
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 100;
    line-height: 37px; /* 148% */
}

.design_center_3_desc_bottom > .title {
    color: #000;
    font-family: Spartan;
    font-size: 49.721px;
    font-style: normal;
    font-weight: 100;
    line-height: 91.155px; /* 183.333% */
    letter-spacing: -3.978px;
}

.design_center_3_desc_bottom > .description {
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 100;
    line-height: 37px; /* 148% */
}

.design_center_4 {
    position: relative;
    background: #FFF;
    width: 100%;
    height: 100vh;
}

.design_center_4 video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.design_center_4_top {
    position: absolute;
    bottom: 10%;
    right: 10%;
    
    
    color: #000;
    text-align: right;
    font-family: Melodrama;
    font-size: 90px;
    font-style: normal;
    font-weight: 200;
    line-height: 94px; /* 104.444% */
}

.design_center_4_bottom {
    display: flex;
    align-items: center;
    padding: 100px 0;
    width: 100%;
}

.design_center_4_bottom div {
    padding: 0 5vw;
}


.design_center_4_bottom > img {
    width: 60%;
}

.design_center_4_bottom_title {
    color: #000;
    text-align: center;
    font-family: Melodrama;
    font-size: 90px;
    font-style: normal;
    font-weight: 500;
    line-height: 110px; /* 122.222% */
}

.design_center_4_bottom_description {
    color: #000;
    text-align: justify;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 100;
    line-height: 32.483px; /* 129.933% */
}
</style>