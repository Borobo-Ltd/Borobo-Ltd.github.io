<template>
    <div class="home">
        <PCHeader/>
        <div class="home_1_bottom">
            <video autoplay loop muted webkit-playsinline playsinline style="">
                <source src="/videos/maah_video_1.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <p style="position: absolute; bottom: 0; width: 100%;">A new Era for home robotics</p>
        </div>
        <div class="home_2">
            <div class="home_2-inner">
                <p class="title" style="letter-spacing: 6px;">What We Do</p>
                <p class="description">Konpanion, offers an alternative and an opportunity in the care, well-being and assistive technology markets, tackling key challenges and offering novel solutions.
                    <br><br>
                    Our focus on building Konpanion as a holistic lifestyle brand creates endless possibilities for expansion and adaptation through its ecosystem of integrated apps and the introduction of personalization, design options, and accessories.
                </p>
            </div>
        </div> 
        <div class="home_3">
            <div class="home_3-inner">
                <p class="title">Maah</p>
                <div style="height: 60px;"></div>
                <p class="description">Drawing inspiration from interior design, nature and art, Maah is our first soft companionship robot; a true hybrid being that realises the promise of form-meets-function with intelligence and grace.
                    <br><br>
                    Powered by a newly-developed AI system capable of learning and expressing meaningful emotions through body language and sound, Maah replicates animal empathy beautifully. Unlike robots that offer poor attempts at conversation, Maah plays with your senses and bonds with humans through more natural, non-verbal communication.</p>
            </div>
        </div>
        <div class="home_4">
            <div class="home_4-inner">
                <div style="height: 100px;"></div>
                <p class="title">OUR PILLARS</p>
                <div style="height: 100px;"></div>
                <div class="home_4_section_container">
                    <div class="home_4_section">
                        <img src="../../assets/images/pillar_1.png" alt="">
                        <p class="home_4_section--title">Powered by Technology.</p>
                        <p class="home_4_section--description">Maah combines the elegance of soft robotics with a unique cognitive architecture, allowing for a vibrant range of expression of emotions and a large range of authentic behaviours. As a true digital native, Maah provides its digital-twin with meaningful information from carefully selected sensors.</p>
                    </div>
                    <div class="home_4_section">
                        <img src="../../assets/images/pillar_2.png" alt="">
                        <p class="home_4_section--title">Driven by Design.</p>
                        <p class="home_4_section--description">Konpanion is an interior design brand using robotics as a means for lifelike design. We aim to build desirable artefacts, in a true tradition of craftsmanship. We hope to make robotics more humane, and sustainable to improve the well-being and trust of all humanity.</p>
                    </div>
                    <div class="home_4_section">
                        <img src="../../assets/images/pillar_3.png" alt="">
                        <p class="home_4_section--title">Grounded in Research.</p>
                        <p class="home_4_section--description">Our focus is to create a personalised and lively companion robot. We are refining its functionalities with the help of our partners in assistive care and research, to provide the best experience for a wide range of users. </p>
                    </div>
                </div>
            </div>
            <div style="height: 140px;"></div>
        </div>
        <div class="home_5">
            <div class="home_5_tile">
                <div class="home_5_title_article">
                    <p class="title" style="text-align: right; font-family: Melodrama; font-style: medium;">a new breed of  <br> companions</p>
                    <p class="description" style="padding-top: 50px; text-align: right; font-style: light;">Through its unique cognitive architecture  Maah is able to replicate animalistic  behaviour and is capable of expressing  emotion akin to a domestic pet</p>
                </div>
                <img src="../../assets/images/tile_1.png" alt="">
            </div>
            <div class="home_5_tile" style="flex-direction: row-reverse;">
                <div class="home_5_title_article" >
                    <p class="title">wellbeing <br> at our core </p>
                    <p class="description" style="padding-top: 50px;">Maah provides companionship to  alleviate loneliness while providing  users with meaningful data through  non-invasive sensing, providing a  unique opportunity for well-being  monitoring and personalized  recommendations to the user. </p>
                </div>
                <img src="../../assets/images/tile_2.png" alt="">
            </div>
            <div class="home_5_tile">
                <div class="home_5_title_article">
                    <p class="title" style="text-align: right;">where craft & technology meet</p>
                    <p class="description" style="padding-top: 50px; text-align: right;">Maah is a made-to-measure robot, challenging traditional mass manufacturing methods. Using the capacity of Industry 4.0 we are aiming to create robot companions uniquely crafted for each user, reducing waste and minimizing the environmental impact of our production processes.</p>
                </div>
                <img src="../../assets/images/tile_3.png" alt="">
            </div>
        </div>
        <img src="../../assets/images/maah_2.png" alt="" width="100%" class="home_6_img">
        <div class="home_6">
            <div style="height: 90px;"></div>
            <div class="home_6_bar"></div>
            <div style="height: 90px;"></div>

            <p class="title">TAILORED TO <span style="font-weight: 200;">YOUR</span> HOME</p>
            <div style="height: 55px;"></div>
            <p class="description" style="font-weight: light; text-align: center;">The robe for Maah is unique in the robotic world. We are combining softness, textures and artistic features to enhance the living experience with your little companion. Similar to the body of Maah, each skin is made individually, allowing special orders to be made. We want to be sure that Maah will fit the aesthetics of your home.</p>
            <div style="height: 55px;"></div>
            
            <video autoplay loop muted webkit-playsinline playsinline style="width: 100%;">
                <source src="/videos/hawick.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>

        <div style="height: 100px; background-color: white;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import PCHeader from '../headers/PCHeader.vue'
// import BackgroundVideo from '../media/BackgroundVideo.vue'

export default {
    name: 'PCHome',
    components: {
        PCHeader,
    },
    // Your Vue component logic goes here
}
</script>

<style scoped>

.title {
    color: #282B46;
    font-family: Spartan;
    font-size: 60px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 6px;
}

.description {
    color: #000;
    font-family: Spartan;
    font-size: 18px;
    font-style: normal;
    font-weight: 300;
    line-height: 25px; /* 138.889% */
}

.home {
    background: #FDF9F3;
}


.home_1_top {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.home_1_top > img {
    width: 320px;
    padding: 70px 0 85px;
}

.home_1_container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0 10%;
}

.home_1_bottom {
    position: absolute; 
    top: 0;
    left: 0;
    width: 100%; 
    height: 100dvh;
}

.home_1_bottom video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.home_1_bottom p {
    color: #FDF9F3;
    text-align: center;
    font-family: Melodrama;
    font-size: 30px;
    font-style: italic;
    font-weight: 500;
    line-height: 25px; /* 83.333% */
    letter-spacing: 3px;
    padding-bottom: 80px;
}

.home_1 h1 {
    color: #fff;
    font-size: 4rem;
}

.navigation_bar {
    display: flex;
    justify-content: center;
    gap: 5vw;
}

.navigation_bar li a {
    padding: 10px;
    text-align: center;
    font-family: Spartan;
    font-size: 16px;
    font-style: normal;
    font-weight: 300;
    line-height: 25px; /* 156.25% */
    letter-spacing: 1.6px;
}


.home_2 {
    display: flex;
    align-items: center;
    justify-content: space-evenly; /* 수평 가운데 정렬 */
    width: 100%;
    position: relative;
    padding-top: calc(100dvh + 237px);
}

.home_2 p {
    align-self: flex-start; /* 아이템들을 상단에 정렬 */
}


.home_2-inner {
    display: flex;
    padding: 0 10%;
    justify-content: space-evenly;
    align-items: space-evenly;
}

.home_2-inner p {
    width: 50%;
}




.home_3 {
    background: url("../../assets/images/maah_1.png") lightgray 50% / cover no-repeat;
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: end;
}

.home_3-inner {
    display: flex;
    flex-direction: column;
    padding-left: 65%;
    padding-right: 5%;
}

.home_4 {
    background: #FFF;
    width: 100%;
    display: flex;
    flex-direction: column;
}

.home_4_section {
    width: 30%;
}

.home_4-inner {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.home_4_section > img {
    width: 100%;
    
}

.home_4_section_container {
    display: flex;
    justify-content: center;
    gap: 2vw;
}

.home_4_section--title {
    color: #000;
    font-family: Spartan;
    font-size: 30px;
    font-style: normal;
    font-weight: semi-bold;
    line-height: 45px; /* 90% */
    letter-spacing: 1.5px;
    margin: 70px 0 40px;
}

.home_4_section--description {
    color: #282B46;
    font-family: Spartan;
    font-size: 18px;
    font-style: light;
    font-weight: 300;
    line-height: 30px; /* 166.667% */
    letter-spacing: 0.9px;
}


.home_5_tile {
    display: flex;
    align-items: center;
}

.home_5_tile > .home_5_title_article > p:first-child {
    font-family: Melodrama;
}

.home_5_tile > * {
    width: 50%;
}

.home_5_tile:nth-child(2) {
    flex-direction: row-reverse;
}


.home_5_title_article {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 0 10%;
}


.home_6 {
    background: #FFF;
    width: 100%;
    padding: 0 10%;
}

.home_6_bar {
    width: 9px;
    height: 61px;
    background: #2F304D;
    margin: 0 auto;
}

.home_6 p {
    padding: 0 10%;
}
</style>