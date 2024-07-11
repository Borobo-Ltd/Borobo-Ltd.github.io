<template>
    <div class="wrapper">
        <m-header />
        <section class="design_container_1">
            <p class="page_title" style="font-weight: 700;">Design-</p>
            <p class="page_title" >Centred</p>
        </section>
        <section class="design_container_2">
            <p class="description">
                We’re on a mission to bring companion robots into homes everywhere. We believe that Maah is the perfect blend of form and function, acting both as a stylish piece of interior design and a beloved pet.
                <br><br>
                As a brand, we are ruling for a new aesthetic in opposition to the current state of robotics. Maah is the result of co-creation and participatory design with our communities.
            </p>
        </section>

        <section class="design_container_3">
            <p>Boundless</p>
            <p>Possibilities</p>
        </section>

        <div style="height: 60px"></div>

        <section class="design_container_4">
            <p class="title">
                THE 
                <br>HIGHLANDS
                <br>RANGE
            </p>
            <div style="height: 20px"></div>
            <p class="description">
                Designed , sourced, developed and manufactured in Scotland, using natural yarns from the Shetland Islands. 
            </p>
        </section>

        <div style="height: 40px"></div>

        <!-- <section class="design_center_3_mobile_inner">
            <div class="design_center_3_desc_mobile">
                <img src="../../assets/images/maah_chair_1.png" width="290px">
                <p class="">MOOSKIT</p>
                <p class="">From the Shetland Islands</p>
            </div>
            <div class="design_center_3_desc_mobile">
                <img src="../../assets/images/maah_chair_2.png" width="290px">
                <p class="">SHOLMIT</p>
                <p class="">From the Shetland Islands</p>
            </div>
            <div class="design_center_3_desc_mobile">
                <img src="../../assets/images/maah_chair_3.png" width="290px">
                <p class="">EESIT</p>
                <p class="">From the Shetland Islands</p>
            </div>
        </section> -->
        <flickity-slider />
        
        <div style="height: 95px"></div>

        <section class="design_container_5">
            <p class="subtitle">behind</p>
            <p class="title">THE COLLECTION</p>
            <p class="description">the first collection highlights our ambition to create another model of 
                development for companion robots. where aesthetics meets sustainability 
                and craft. <br><br> Our robots are crafted using cutting-edge textile development 
                methods, rather than traditional rigid plastic exteriors. This not only elevates
                the aesthetic of Maah but also allows us to take a more responsible approach
                to their development. <br><br> We believe that this new development model will not
                only improve the positive impact of our technology but also enhance the bond 
                between you and your companion robot.</p>
        </section>


        <section class="design_container_6">
            <video autoplay loop muted webkit-playsinline playsinline width="100%">
                <source src="/videos/maah_video_3.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <p class="text">
                A companion
                <br> matching your
                <br> <span style="font-weight: 500; font-family: Melodrama;">unique</span> style
            </p>
        </section>
        <section class="design_container_7">
            <img src="../../assets/images/maah_chair_4.png" alt="">
            <div>
                <p class="title" style="padding: 35px 0;">Adaptability by 
                    <br> Design</p>
                <p class="description">Even if turned off, Maah will still live and exist in your personal space. It is designed to fit your tastes and blend in or stand out in your environment. Maah is interior design as a means , not an end</p>
            </div>
        </section>

        <img src="../../assets/images/footer.png" alt="" width="100%">

    </div>
</template>

<script>

import MHeader from '../headers/MHeader.vue';
import FlickitySlider from './FlickitySlider.vue';


export default {
    components: {
        MHeader,
        FlickitySlider
    },
}
</script>

<style scoped>
.wrapper {
    background: #FDF9F3;
}

.description {
    color: #282B46;
    font-family: Spartan;
    font-size: 15px;
    font-style: normal;
    font-weight: 300;
    line-height: 22px; /* 146.667% */
}

.design_container_1 {
    padding: 0 10%;
    background: url(../../assets/images/artwork_1.png) no-repeat;
    background-size: cover;
    width: 100%;
    height: 635px;
    
}

.design_container_2 {
    padding: 0 10%;
}

.design_container_3 {
    background: url(../../assets/images/maahs.png) no-repeat;
    background-size: cover;
    width: 100%;
    height: 503px;
    padding: 10%;
}

.design_container_3 p {
    color: #282B46;
    text-align: right;
    font-family: Melodrama;
    font-size: 40px;
    font-style: normal;
    font-weight: 500;
    line-height: 91%; /* 36.4px */
    letter-spacing: -0.8px;
}

.design_center_3_desc_mobile > *:nth-child(2) {
    color: #000;
    font-family: Spartan;
    font-size: 16.258px;
    font-style: normal;
    font-weight: 300;
    line-height: 24.061px; /* 148% */
    padding-top: 25px;
}

.design_center_3_desc_mobile > *:nth-child(3) {
    color: #000;
    font-family: Spartan;
    font-size: 13.006px;
    font-style: normal;
    font-weight: 300;
    line-height: 24.061px; /* 185% */
}

.design_container_4 {
    padding: 0 10%;
}

.design_container_4 > .title {
    color: #000;
    font-family: Spartan;
    font-size: 45px;
    font-style: normal;
    font-weight: 250;
    line-height: 55px; /* 122.222% */
    letter-spacing: -3.6px;
}

.design_center_3_mobile_inner {
    display: flex;
    gap: 5%;
    width: 100%;
    position: relative;
    overflow: hidden;
}

.design_center_3_desc_mobile {
    position: relative;
    left: calc((100vw - 870px)/2 - 5%);
    flex-shrink: 0;
}

.design_center_3_desc_mobile img {
    height: auto;
    width: 290px;
}

.design_container_5 {
    padding-top: 95px;
    padding: 95px 10% 60px 10%;
}

.design_container_5 > .subtitle {
    color: #000;
    font-family: Spartan;
    font-size: 18.421px;
    font-style: normal;
    font-weight: 250;
    line-height: 27.263px; /* 148% */
}

.design_container_5 > .title {
    color: #000;
    font-family: Spartan;
    font-size: 34px;
    font-style: normal;
    font-weight: 250;
    line-height: 67.167px; /* 197.549% */
    letter-spacing: -2.72px;
    padding-bottom: 25px;
}

.design_container_5 > .description {
    color: #000;
    text-align: justify;
    font-family: Spartan;
    font-size: 15.957px;
    font-style: normal;
    font-weight: 250;
    line-height: 23.935px; /* 150% */
}


.design_container_6 {
    position: relative;
    width: 100%;
    height: 503px;
    padding: 10%;
}

.design_container_6 > video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}


.design_container_6 > .text {
    position: absolute;
    bottom: 10%;
    right: 10%;
    color: #000;
    text-align: right;
    font-family: Spartan;
    font-size: 34px;
    font-style: normal;
    font-weight: 250;
    line-height: 30px; /* 88.235% */
    letter-spacing: -2.72px;
}

.design_container_7 {
    padding: 20%;
}

.design_container_7 .title {
    color: #000;
    text-align: center;
    font-family: Melodrama;
    font-size: 34px;
    font-style: normal;
    font-weight: 500;
    line-height: 43.505px; /* 127.957% */
}
</style>
