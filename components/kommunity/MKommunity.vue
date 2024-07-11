<template>
    <div style="background-color: #FDF9F3;">
        <MHeader />
        <div :class="$style.container_1">
            <p class="page_title" style="font-size: 16px; font-weight: 300; color: #282B46;">coming soon...</p>
            <img src="../../assets/images/kommunity.png" alt="">
            <p class="page_title" style="font-size: 40px; font-weight: 300; color: #282B46; text-align: left; width: 100%;">‘We don’t heal <br>in isolation,</p>
            <div style="height: 25px;"></div>
            <p class="page_title" style="font-size: 40px; font-weight: 300; color: #282B46; text-align: right; width: 100%;">but in <br> community’</p>
            <div style="height: 115px;"></div>
            <p :class="$style.description">Kommunity will be a space focused on lifestyle and well-being, where our users will be able to join a global community in which to get inspiration, learn and share their stories. </p>
        </div>
        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import MHeader from '../headers/MHeader.vue';
export default {
    name: 'MKommunity',
  components: { MHeader },
};
</script>

<style module>
/* Your component styles go here */
.container_1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: #FDF9F3;
    padding: 0 10%;
}

.description {
    color: #282B46;
    text-align: justify;
    font-family: Spartan;
    font-size: 16px;
    font-style: normal;
    font-weight: 300;
    line-height: 22px; /* 137.5% */
}
</style>