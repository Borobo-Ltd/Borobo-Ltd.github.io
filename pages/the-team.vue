<template>
    <div>
        <PCTheTeam class="pc"/>
        <MTheTeam class="mobile"/>
    </div>
</template>

<script>
import PCTheTeam from '../components/theTeam/PCTheTeam.vue';
import MTheTeam from '../components/theTeam/MTheTeam.vue';

export default {
    components: {
        PCTheTeam,
        MTheTeam,
    }
}
</script>