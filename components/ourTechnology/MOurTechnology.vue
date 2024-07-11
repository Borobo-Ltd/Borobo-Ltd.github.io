<template>
    <div class="wrapper">
        <section>
            <div class="video">
                <div class="additional_space"></div>
                <video autoplay loop muted webkit-playsinline playsinline >
                    <source src="/videos/maah_video_2.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
            </div>
            <div class="container">
                <MHeader :is-dark="true" />
                <div class="our_technology_container">
                    <p class="page_title" style="font-weight: 400;">Our</p>
                    <p class="page_title" style="font-weight: 700;">Technology</p>
                    <div class="technology_description_container">
                        <p class="description technology_text">
                            Unlike robots with limited conversational skills, Maah bonds with you through natural, non-verbal communication.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <section class="container_2">
            <div style="height: 50px;"></div>
            <TechnologyParagraph 
                :title="title1"
                :description="description1"
                color="#FDF9F3"
                text-align="right"
            />
            <img src="../../assets/images/maah_sketch_1.png" alt="">
            <div style="height: 40px;"></div>
            <TechnologyParagraph 
                :title="title2"
                :description="description2"
                color="#FDF9F3"
            />
            <img src="../../assets/images/maah_sketch_2.png" alt="">

            <img src="../../assets/images/maah_sketch_3.png" alt="">
            <TechnologyParagraph 
                :title="title3"
                :description="description3"
                color="#FDF9F3"
            />
        <div style="height: 40px;"></div>

        </section>

        <div style="height: 40px;"></div>
        <section class="container_3">
            <TechnologyParagraph 
            :title="title4"
            :description="description4"
            color="#2F304D"
            />
        </section>
        <div style="height: 40px;"></div>

        <img src="../../assets/images/user_interface.png" alt="" style="padding: 0 5%;">

        
        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">

    </div>
</template>

<script>

import MHeader from '../headers/MHeader.vue';
import TechnologyParagraph from './TechnologyParagraph.vue';


export default {
    components: {
        MHeader,
        TechnologyParagraph
    },
    data() {
        return {
            title1: 'Non-invasive \n sensing',
            description1: 'Unlike other devices that rely on cameras, Maah’s non-invasive sound sensors offer a unique privacy-focused approach to assistive technology. Ensuring that users privacy is respected while still providing customized health monitoring. Its potential to integrate with other IoT systems further enhances its capabilities, making it an innovative and effective addition to any home.',
            title2: 'Cognitive\nArchitecture',
            description2: 'Our proprietary technology, developed over the last 10 years, allows non-linear behaviour to emerge, creating a sense of a real living entity. A breakthrough in lightweight cognitive AI systems, enables a more natural and evolving relationship, allowing each MAAH to develop uniquely alongside their owner.',
            title3: 'Digital Twin',
            description3: 'Maah gathers information from its real-world environment and, if wished for by the user, translates it to its Digital Twin: a mirror image of your Maah that exists purely in a virtual space.\n\n\nThis doppelganger allows the primary and other selected users to access such information. From checking in on your loved ones to providing updates to medical practitioners and carers.',
        
            title4: 'Digital\nEnvironment',
            description4: "At the start, the digital twin exists in a homely surreal digital environment, accompanied by a dashboard in which real-world data obtained from Maah's sensors is visualised in real-time for their users to interact with.\n\nIn Konpanion+ this data can be shared with the user's medical practitioner for a more tailored health tracking and diagnosis approach.",
        }
    },
}
</script>

<style lang="css" scoped>
    img {
        width: 100%;
        height: auto;
    }

    .wrapper {
        position: relative;
    }

    .additional_space {
        width: 100%;
        height: 50dvh;
        background-color: #EBF2F8;
    }

    video {
        width: 100%;
        height: 50dvh;
        object-fit: cover;
    }

    .video img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .container {
        position: absolute;
        top: 0;
    }

    .our_technology_container {
        padding: 0 10%;
    }

    .description {
        color: #2F304D;
        font-family: Spartan;
        font-size: 17px;
        font-style: normal;
        font-weight: 200; /* 올바른 font-weight 값으로 수정 */
        line-height: 22px; /* 129.412% */
    }

    .technology_description_container {
        display: flex;
        width: 70%;
        justify-content: end;
    }

    .technology_text {
        padding-top: 40px;
    }

    .container_2 {
        background-color: #2F304D;
    }
</style>
