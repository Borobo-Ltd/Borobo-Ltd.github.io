<template>
    <div>
        <PCWeCare class="pc" />
        <MWeCare class="mobile" />
    </div>
</template>

<script>
import PCWeCare from '../components/weCare/PCWeCare.vue';
import MWeCare from '../components/weCare/MWeCare.vue';
export default {
    components: {
        PCWeCare,
        MWeCare
    }
    // Your component options go here
}
</script>

<style module>
/* Your component styles go here */
</style>