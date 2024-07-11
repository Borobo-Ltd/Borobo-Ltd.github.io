<template>
    <div>
        <PCHeader is-dark is-sticky-header-dark/>
        <section :class="$style.container_1">
            <video autoplay loop muted webkit-playsinline playsinline>
                <source src="/videos/maah_video_2.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; padding: 0 10%;">
                <div style="height: 237px;"></div>
                <p class="page_title" style="font-size: 110px;">Our</p>
                <p class="page_title" style="font-weight: 700; font-size: 110px;">Technology</p>
                <div style="height: 80px;"></div>
                <p :class="$style.description" style="width: 50%;">Powered by a newly-developed AI architecture capable of learning and meaningful expressions (artificial emotions) through body language and sound, Maah beautifully utilizes concepts relating to human empathy.
                Unlike robots that offer poor attempts at conversation, Maah plays with your senses and bonds with you through more natural, non-verbal communication</p>
            </div>
        </section>

        <section :class="$style.container_2">
            <div :class="$style.flex_1">
                <img src="../../assets/images/maah_sketch_1.png" style="flex: 1; width: 65%;">
                <div style="flex: 2;">
                    <p class="page_title" style="font-size: 75px; color: #FDF9F3; text-align: right">
                        Non-invasive 
                        <br>
                        Sensing
                    </p>
                    <div style="height: 110px;"></div>
                    <p :class="$style.description" style="color: #FDF9F3; text-align: right;">
                        Maah's non-invasive sound sensors provide a privacy-focused alternative to traditional assistive technology that relies on cameras. This open, non-threatening approach ensures user privacy while delivering customised health monitoring. Its potential for IoT integration enhances its effectiveness, making Maah an innovative addition to any home.   
                    </p>
                </div>
            </div>
            <div :class="$style.flex_2">
                <div style="flex: 2;">
                    <p class="page_title" style="font-size: 75px; color: #FDF9F3;">
                        Cognitive 
                        <br>
                        Architecture
                    </p>
                    <div style="height: 110px;"></div>
                    <p :class="$style.description" style="color: #FDF9F3;">
                        Maah's non-invasive sound sensors provide a privacy-focused alternative to traditional assistive technology that relies on cameras. This open, non-threatening approach ensures user privacy while delivering customised health monitoring. Its potential for IoT integration enhances its effectiveness, making Maah an innovative addition to any home.   
                    </p>
                </div>
                <div style="width: 10%;"></div>
                <img src="../../assets/images/maah_sketch_2.png" style="flex: 1; width: 55%;">
            </div>
            <div style="padding: 0 15%;">
                <p class="page_title" style="font-size: 75px; color: #FDF9F3; text-align: center;">
                    Digital Twin
                </p>
                <div style="height: 110px;"></div>
                <p :class="$style.description" style="color: #FDF9F3; text-align: center;">
                    Maah's non-invasive sound sensors provide a privacy-focused alternative to traditional assistive technology that relies on cameras. This open, non-threatening approach ensures user privacy while delivering customised health monitoring. Its potential for IoT integration enhances its effectiveness, making Maah an innovative addition to any home.   
                </p>
            </div>
        </section>
        <section :class="$style.container_3">
            <div style="background: #2F304D; height: 50%; width: 100%; position: absolute; z-index: -1;"></div>
            <img src="../../assets/images/maah_sketch_3.png" alt="" width="100%">
        </section>
        <section :class="$style.container_4">
            <p class="page_title" style="font-size: 75px; text-align: center;">
                DIGITAL ENVIRONMENT
            </p>
            <div style="height: 110px;"></div>
            <p :class="$style.description" style="text-align: center; padding: 0 10%;">
                At the start, the digital twin exists in a homely surreal digital environment, accompanied by a dashboard in which real-world data obtained from MAAH's sensors is visualised in real-time for their users to interact with. In Konpanion+ this data can be shared with the user's medical practitioner for a more tailored health tracking and diagnosis approach   
            </p>
        </section>
        <div style="height: 65px;"></div>
        <img src="../../assets/images/user_interface.png" alt="" width="100%" style="padding: 5%;">


        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import PCHeader from '../headers/PCHeader.vue'
export default {
    name: 'PCOurTechnology',
    components: { PCHeader },
    data() {
        return {
            technologies: []
        }
    },
    mounted() {
        // Fetch technologies data from API or perform any necessary initialization here
    },
    methods: {
        // Define any additional methods here
    }
}
</script>

<style module>
.container_1 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100dvh;
    padding: 0 10%;
}

.container_1 video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    margin: 0;
    object-fit: cover;
}

.description {
    color: #2F304D;

/* Body_Full */
    font-family: Spartan;
    font-size: 22px;
    font-style: normal;
    font-weight: 200;
    line-height: 38px; /* 159.091% */
    letter-spacing: 0.88px;
}

.container_2 {
    background: #2F304D;
    padding-top: 100dvh;
}

.flex_1 {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding-right: 10%;
}

.flex_2 {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    padding-left: 10%;
}

.container_3 {
    position: relative;
}

</style>