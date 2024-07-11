<template>
    <div style="background-color: #FDF9F3;">
        <PCHeader is-dark/>
        <div style="height: 237px;"></div>

        <section :class="$style.container_1">
            <div style="width: 40%; flex: 4; margin: 0 auto;">
                <p class="page_title" style="font-size: 100px;">We</p>
                <p class="page_title" style="font-weight: 700; font-size: 100px;">Care</p>
                <p :class="$style.description" style="padding-top: 85px;">
                    We are fully devoted to our community and want to put our technologies and products to improve the well-being of those around us. As a result, we have developed Konpanion+, a dedicated service designed to support the care industry.
                    <br><br>
                    We want as many people as possible to benefit from Maah, get in touch with us! 
                </p>
            </div>
            <div style="width: 5%;"></div>
            <div :class="$style.slideshow">
                <img src="../../assets/images/we_care_1.png" alt="" :class="$style.background">
                <img src="../../assets/images/we_care_2.png" alt="" :class="$style.foreground">
            </div>
        </section>

        <section :class="$style.container_2">
            <div style="display: flex; justify-content: center; flex: 2;">
                <p class="page_title" style="font-size: 64px; line-height: 85px; text-align: right;">
                    A silent
                    <br>
                    fight
                </p>
            </div>
            <p :class="$style.description" style="flex: 3;">
                Loneliness is an epidemic, it increases the chances of chronic illnesses, deteriorates mental health and is increasing amongst all age groups. Social robots can reduce loneliness, however, acceptance of current platforms is not high. 
                <br><br>
                Maah provides both an advanced hardware and software platform to support the health industry to help the users and families regardless of their age or condition.
            </p>
        </section>

        <div style="height: 130px;"></div>

        <p class="page_title" style="font-weight: 400; text-align: center; font-size: 42px; line-height: 60px;">ESTABLISHING A SHARED LANGUAGE <br> WITH USERS</p>

        <div style="height: 130px;"></div>

        <section :class="$style.container_3">
            <div :class="$style.items">
                <img src="../../assets/images/we_care_sketch_1.png" alt="">
                <p>CO-DESIGN APPROACH</p>
                <p>Co-design is at the heart of our process to understand our clients better than anyone else. Supported by research to ensure rigorous and systemic results for a better approach to robotics, care and well-being.</p>
            </div>
            <div :class="$style.items">
                <img src="../../assets/images/we_care_sketch_2.png" alt="">
                <p>CO-DESIGN APPROACH</p>
                <p>Co-design is at the heart of our process to understand our clients better than anyone else. Supported by research to ensure rigorous and systemic results for a better approach to robotics, care and well-being.</p>
            </div>
            <div :class="$style.items">
                <img src="../../assets/images/we_care_sketch_3.png" alt="">
                <p>CO-DESIGN APPROACH</p>
                <p>Co-design is at the heart of our process to understand our clients better than anyone else. Supported by research to ensure rigorous and systemic results for a better approach to robotics, care and well-being.</p>
            </div>
        </section>

        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import PCHeader from '../headers/PCHeader.vue'
export default {
    name: 'PCWeCare',
    components: { PCHeader },
    // Your component logic goes here
}
</script>

<style module>
.container_1 {
    display: flex;
    justify-content: center;
    align-items: stretch;
    padding: 160px 0 0 10%;
}

.container_2 {
    display: flex;
    justify-content: space-around;
    align-items: start;
    padding: 165px 10%;
}

.container_3 {
    display: flex;
    justify-content: space-around;
    align-items: start;
    gap: 5%;
    padding: 0 10%;
}

.description {
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 200;
    line-height: 37px; /* 148% */
}

.items {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 45px;
}

.items > *:nth-child(2) {
    color: #282B46;
    text-align: center;
    font-family: Spartan;
    font-size: 22px;
    font-style: normal;
    font-weight: 700;
    line-height: 33px; /* 150% */
    letter-spacing: 2.64px;
}

.items > *:nth-child(3) {
    color: #282B46;
    text-align: justify;
    font-family: Spartan;
    font-size: 14px;
    font-style: normal;
    font-weight: 300;
    line-height: 22px; /* 157.143% */
}

.slideshow {
    position: relative;
    width: 60%;
    height: auto;
    
}

.slideshow img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.slideshow img.background {
    opacity: 1;
}

.slideshow img.foreground {
    opacity: 0;
    animation: fade 12s infinite;
}

@keyframes fade {
    0% { opacity: 0; }
    25% { opacity: 1; }
    50% { opacity: 1; }
    100% { opacity: 0; }
}
</style>