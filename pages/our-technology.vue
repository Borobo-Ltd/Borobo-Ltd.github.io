<template>
    <div>
        <PCOurTechnology class="pc" />
        <MOurTechnology class="mobile" />
    </div>
</template>

<script>
import PCOurTechnology from '../components/ourTechnology/PCOurTechnology.vue';
import MOurTechnology from '../components/ourTechnology/MOurTechnology.vue';

export default {
    components: {
        PCOurTechnology,
        MOurTechnology,
    }
}
</script>