<template>
    <div>
        <div :class="$style.container">
            <div style="height: 237px;"></div>

            <PCHeader is-dark/>
            <div style="height: 160px;"></div>
            <p class="page_title" style="font-size: 40px; color: #282B46; font-weight: 300;">coming soon...</p>
            <img src="../../assets/images/kommunity.png" alt="">
            <p class="page_title" style="font-size: 65px; color: #282B46; text-align: center;">‘We don’t heal in isolation,
                <br>
                but in community’</p>
            <div style="height: 30px;"></div>
            <p class="page_title" style="font-size: 40px; color: #282B46; font-weight: 300; text-align: center;">- S. Kelley Harrell</p>
            <div style="height: 105px;"></div>
            <p class="page_title" style="font-size: 25px; color: #282B46; font-weight: 300; width: 60%;">Kommunity will be a space focused on lifestyle and well-being, where our users will be able to join a global community in which to get inspiration, learn and share their stories. </p>
            <div style="height: 100px;"></div>
            <img src="../../assets/images/footer.png" alt="" width="100%">
        </div>
        
    </div>
</template>

<script>
import PCHeader from '../headers/PCHeader.vue'
export default {
    name: 'PCKommunity',
    components: { PCHeader },
}
</script>

<style module>
.container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #FDF9F3;    
}

</style>