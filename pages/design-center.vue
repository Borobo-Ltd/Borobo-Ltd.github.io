<template>
    <div>
        <PCDesignCenter class="pc" />
        <MDesignCenter class="mobile" />
    </div>
</template>

<script>
import PCDesignCenter from '../components/designCetner/PCDesignCenter.vue';
import MDesignCenter from '../components/designCetner/MDesignCenter.vue';

export default {
    components: {
        PCDesignCenter,
        MDesignCenter
    }
}
</script>