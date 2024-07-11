<template>
        <div>
          
          <section class="container_1">
            <video autoplay loop muted webkit-playsinline playsinline style="">
                <source src="/videos/maah_video_1.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>

            <div style="display: flex; width: 100%; height: 100%; position: absolute; top: 0; left: 0; justify-content: center;">
              <img src="../../assets/logos/logo_white.svg" alt="" width="210px">
            </div>

            <MHeader :is-dark="false" :is-logo="false"  style="position: absolute; top: 0; left: 0; width: 100%;"/>
      
            <p style="position: absolute; bottom: 0; width: 100%;">A new Era for home robotics</p>
          </section>
      
          <section class="container_2">
            <p>What</p>
            <p>we do</p>
            <div style="height: 40px;"></div>
            <p class="description">Konpanion, offers an alternative and an opportunity in the care, well-being and assistive technology markets, tackling key challenges and offering novel solutions.
            <br><br>
            Our focus on building Konpanion as a holistic lifestyle brand creates endless possibilities for expansion and adaptation through its ecosystem of integrated apps and the introduction of personalization, design options, and accessories.</p>
          </section>
      
          <section class="container_3">
            <p class="page_title" style="font-weight: 300;">Meet</p>
            <p class="page_title" style="font-weight: 500;">Maah</p>
          </section>
      
          <section class="container_4">
            <p class="description">
              Drawing inspiration from interior design, nature, and craft, Maah is our first soft companion robot, embodying form-meets-function with intelligence and grace. 
              <br><br>
              Powered by advanced AI, Maah learns and expresses meaningful emotions through body language and sound, beautifully replicating animal empathy. 
              <br><br>
              Unlike robots with limited conversational skills, Maah bonds with humans through natural, non-verbal communication. 
            </p>
          </section>
      
          <div style="height: 90px;"></div>
      
          <section class="container_5">
            <p class="page_title">OUR PILLARS</p>
            <m-home-item 
            v-for="item in items" 
            :key="item.name"
            :name="item.name" 
            :description="item.description" 
            :image="item.image" 
            />
          </section>
      
          <div style="height: 90px;"></div>
      
          <section class="container_6">
            <div class="tile tile_img_1">
              <div class="tile_container_1">
                <p>a new breed of companions</p>
                <p style="width: 80%;">Through its unique and proprietary cognitive architecture Maah is able to replicate animal-like behaviour, capable of expressing emotion akin to a domestic pet.</p>
              </div>
            </div>
      
            <div class="tile tile_img_2">
              <div class="tile_container_2">
                <p>wellbeing at our core</p>
                <p>Our design team has created a range of accessories and customisations to make Maah truly yours. From different colours to unique patterns, Maah can be tailored to your style.</p>
              </div>
            </div>
      
            <div class="tile tile_img_3">
              <div class="tile_container_3">
                <p>where craft & <br> technology meet</p>
                <p>Maah is a made-to-measure robot, challenging traditional mass manufacturing methods. Using the capacity of Industry 4.0 we are aiming to create robot companions uniquely crafted for each user, reducing waste and minimizing the environmental impact of our production processes.</p>
              </div>
            </div>
          </section>
      
          <section class="container_7">
            <img src="../../assets/images/maah_2.png" alt="" width="100%" class="home_6_img">
              <div class="home_6">
                  <div style="height: 20px;"></div>
                  <div class="home_6_bar"></div>
                  <div style="height: 20px;"></div>
      
                  <p class="title">TAILORED TO <span style="font-weight: 100;">YOUR</span> HOME</p>
                  <div style="height: 55px;"></div>
                  <p class="description">The robe for Maah is unique in the robotic world. We are combining softness, textures and artistic features to enhance the living experience with your little companion. Similar to the body of Maah, each skin is made individually, allowing special orders to be made. We want to be sure that Maah will fit the aesthetics of your home.</p>
                  <div style="height: 55px;"></div>
                  <video autoplay loop muted webkit-playsinline playsinline style="width: 100%;">
                      <source src="/videos/hawick.mp4" type="video/mp4">
                      Your browser does not support the video tag.
                  </video>
              </div>
          </section>


        <div style="height: 100px;"></div>
        <img src="../../assets/images/home_footer.png" alt="" width="100%">
    </div>
  
  
  </template>
  
  <script>
import MHeader from '../headers/MHeader.vue';
import MHomeItem from './MHomeItem.vue';
  
  export default {
    name: 'MHome',
    components: {
      MHeader,
      MHomeItem
    },
    data() {
      return {
        items: [
          {
            name: 'Powered by Technology.',
            description: 'Maah combines the elegance of soft robotics with a unique cognitive architecture, allowing for a vibrant range of expression of emotions and a large range of authentic behaviours. As a true digital native, Maah provides its digital-twin with meaningful information from carefully selected sensors.',
            image: 'pillar_1'
          },
          {
            name: 'Driven by Design',
            description: 'Konpanion is an interior design brand using robotics as a means for lifelike design. We aim to build desirable artefacts, in a true tradition of craftsmanship. We hope to make robotics more humane, and sustainable to improve the well-being and trust of all humanity.',
            image: 'pillar_2'
          },
          {
            name: 'Grounded in Research',
            description: 'Our focus is to create a personalised and lively companion robot. We are refining its functionalities with the help of our partners in assistive care and research, to provide the best experience for a wide range of users.',
            image: 'pillar_3'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .container_1 {
    position: relative;
    width: 100%;
    height: 100vh;
  }

  .container_1 video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100dvh;
    object-fit: cover;
  }
  
  .container_1 p {
    color: #FDF9F3;
    text-align: center;
    font-family: Melodrama;
    font-size: 18.028px;
    font-style: italic;
    font-weight: 500;
    line-height: 15.023px; /* 83.333% */
    letter-spacing: 1.803px;
    padding-bottom: 60px;
  }
  
  .container_2 {
    padding: 10% 10% 0 10%;
    background: #FDF9F3;
  }
  
  .container_2 p:nth-child(1), .container_2 p:nth-child(2) {
    color: #282B46;
    font-family: Spartan;
    font-size: 45px;
    font-style: normal;
    font-weight: 400;
    line-height: 112.078%; /* 50.435px */
    letter-spacing: -0.9px;
  }
  
  .description {
    color: #282B46;
  
    /* Body */
    font-family: Spartan;
    font-size: 15px;
    font-style: normal;
    font-weight: 300;
    line-height: 25px; /* 166.667% */
  }
  
  .container_3 {
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: end;
    padding: 10%;
    background: url(../../assets/images/maah_1.png) no-repeat;
    height: 550px;
    width: 100%;
    background-size: cover;
  }
  
  .container_4 {
    padding: 0 10%;
  }
  
  .container_5 {
    padding: 0 15%;
  }
  
  .tile {
    background-size: contain;
    width: 100%;
    height: 503px;
  }
  
  .tile_container_1 {
    padding: 10%;
    border-radius: 5px 0px 0px 5px;
    background: rgba(77, 36, 36, 0.70);
  }
  
  .tile_container_2 {
    position: relative;
    top: 5%;
    padding: 10%;
    border-radius: 0px 5px 5px 0px;
    background: rgba(102, 57, 36, 0.60);
    width: 70%;
  }
  
  .tile_container_3 {
    position: relative;
    top: 10%;
    padding: 10%;
    border-radius: 5px 0px 0px 5px;
    background: rgba(77, 36, 36, 0.70);
  }
  
  .tile p:first-child {
    color: #FFF;
    font-family: Melodrama;
    font-size: 34px;
    font-style: normal;
    font-weight: 500;
    line-height: 27px; /* 79.412% */
    text-transform: lowercase;
  }
  
  .tile p:nth-child(2) {
    color: #FFF;
    text-align: justify;
    font-family: Spartan;
    font-size: 13px;
    font-style: normal;
    font-weight: 300;
    line-height: 17px; /* 130.769% */
    letter-spacing: 0.65px;
    padding-top: 20px;
  }
  
  .tile_img_1 {
    background: url(../../assets/images/tile_1.png) no-repeat;
    padding: 5% 0 0 5%;
    background-size: cover;
  }
  
  .tile_img_2 {
    background: url(../../assets/images/tile_2.png) no-repeat;
    background-size: cover;
  }
  
  .tile_img_3 {
    background: url(../../assets/images/tile_3.png) no-repeat;
    padding-left: 5%;
    background-size: cover;
  }
  
  .home_6 {
    padding: 0 15%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  
  .home_6 .title {
    color: #282B46;
    text-align: center;
    font-family: Spartan;
    font-size: 20px;
    font-style: normal;
    font-weight: 300;
    line-height: 22.396px; /* 128.571% */
  }
  
  .home_6_img {
      padding: 5%;
  }
  
  .home_6_bar {
      width: 1vw;
      height: 6vw;
      background: #282B46;
      flex-shrink: 0;
  }
  
  /* 
  .tile_2 {
    background: url(../../assets/images/tile_2.png) no-repeat;
    background-size: cover;
    width: 100%;
    height: 503px;
  }
  
  .tile_3 {
    background: url(../../assets/images/tile_3.png) no-repeat;
    background-size: cover;
    width: 100%;
    height: 503px;
  } */
  
  </style>