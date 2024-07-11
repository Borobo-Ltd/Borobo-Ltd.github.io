<template>
    <div style="background-color: #FDF9F3;">
        <m-header />
        <section :class="$style.container_1">
            <p class="page_title">We</p>
            <p class="page_title" style="font-weight: 700;">Care</p>
            <div style="height: 90px;"></div>
            <p :class="$style.description">We are fully devoted to our community and want to put our technologies and products to improve the well-being of those around us. As a result, we have developed Konpanion+, a dedicated service designed to support the care industry.
                <br><br>
            Contact us to get involved or learn more.</p>
        </section>
        <div style="height: 65px;"></div>
        <div :class="$style.slideshow">
            <img src="../../assets/images/we_care_1.png" alt="" :class="$style.background">
            <img src="../../assets/images/we_care_2.png" alt="" :class="$style.foreground">
        </div>
        <div style="height: 80px;"></div>
        
        <section :class="$style.container_1">
            <p class="page_title" style="text-align: right;">A silent
                <br>
                fight</p>
            <div style="height: 50px;"></div>
            <p :class="$style.description">Loneliness is an epidemic, it increases the chances of chronic illnesses, deteriorates mental health and is increasing amongst all age groups. Social robots can reduce loneliness, however, acceptance of current platforms is not high. 
                <br><br>
                Maah provides both an advanced hardware and software platform to support the health industry to help the users and families regardless of their age or condition.</p>
        </section>
        <div style="height: 70px;"></div>
        <p class="page_title" style="font-weight: 400; text-align: center; font-size: 25px;">ESTABLISHING A <br> SHARED LANGUAGE <br> WITH USERS</p>
        
        <div style="height: 70px;"></div>
        <section :class="$style.container_1">
            <div :class="$style.flex">
                <img src="../../assets/images/we_care_sketch_1.png" alt="">
                <p>CO-DESIGN<br>APPROACH</p>
                <p>Co-design is at the heart of our process to understand our clients better than anyone else. Supported by research to ensure rigorous and systemic results for a better approach to robotics, care and well-being.</p>
            </div>
            <div :class="$style.flex">
                <img src="../../assets/images/we_care_sketch_2.png" alt="">
                <p>TAILORED<br>EXPERIENCE</p>
                <p>Maah offers a range of sensors to widen its perception of the world. With the help of care provider specialists, we can identify specific patterns to support patients and carers in a meaningful way.</p>
            </div>
            <div :class="$style.flex">
                <img src="../../assets/images/we_care_sketch_3.png" alt="">
                <p>PEOPLE<br>CENTRED</p>
                <p>With the help of our users and experts in design research, we are focusing on making the experience of Maah as seamless as possible. Technology should be simple to use for every demographic while providing joy and meaningful interactions.</p>
            </div>
        </section>
        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import MHeader from '../headers/MHeader.vue'
export default {
    name: 'MWeCare',
    components: {
        MHeader
    }   
}
</script>

<style module>
.container_1 {
    padding: 0 10%;
}

.flex {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
}

.flex > *:nth-child(2) {
    color: #282B46;
    text-align: center;
    font-family: Spartan;
    font-size: 22px;
    font-style: normal;
    font-weight: 700;
    line-height: 33px; /* 150% */
    letter-spacing: 2.64px;
    padding: 50px 0;
}

.flex > *:nth-child(3) {
    color: #282B46;
    font-family: Spartan;
    font-size: 14px;
    font-style: normal;
    font-weight: 300;
    line-height: 22px; /* 157.143% */
}

.description {
    color: #282B46;
    font-family: Spartan;
    font-size: 16px;
    font-style: normal;
    font-weight: 300;
    line-height: 25px; /* 156.25% */
}


.slideshow {
    position: relative;
    width: 100%;
    height: 100vw;
    
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