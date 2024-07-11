<template>
    <div>
        <PCKommunity class="pc" />
        <MKommunity class="mobile" />
    </div>
</template>

<script>
import PCKommunity from '../components/kommunity/PCKommunity.vue';
import MKommunity from '../components/kommunity/MKommunity.vue';

export default {
    components: {
        PCKommunity,
        MKommunity,
    }
}
</script>